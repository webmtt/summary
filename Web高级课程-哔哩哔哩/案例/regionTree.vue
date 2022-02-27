<template>
  <div style="height: calc(100% - 50px); padding-top: 10px">
    <el-input
      v-if="ifShowSearch"
      v-model="inputValue"
      placeholder="请输入关键字"
      class="filter-tree-input"
      style="padding-bottom: 10px"
      suffix-icon="h-icon-search"
      clearable
      :on-icon-click="handleInputClick"
      :clear-icon-click="clearIconClick"
      @keyup.enter.native="handleInputClick"
    ></el-input>
    <el-tree
      v-if="!ifSearch"
      ref="simpleTree"
      :data="treeData"
      :props="defaultProps"
      simple-data
      :load="loadNode"
      :lazy="true"
      node-key="deptIndexCode"
      parent-key="parentIndexCode"
      :current-node-key="currentNode.deptIndexCode"
      :default-expand-all="false"
      show-checkbox
      :show-checkbox="ifShowCheckbox"
      @current-change="currentChange"
      @check-change="handleCheckChange"
    />
    <el-tree
      v-if="ifSearch"
      :data="treeDataSearch"
      :props="defaultProps"
      :default-expanded-keys="['view', 'preview', 'videoPlayBack']"
      show-checkbox
      node-key="deptIndexCode"
      parent-key="parentIndexCode"
      @check="checkChange"
    />
  </div>
</template>

<script>
import { queryChildDept, queryPerson, deptqueryTree } from '@/api/index'
export default {
  props: {
    type: { type: String, default: 'dept' },
    ifShowCheckbox: {
      type: Boolean,
      default: true,
    },
    ifShowSearch: {
      type: Boolean,
      default: false,
    },
  },
  data() {
    return {
      inputValue: '',
      treeDataSearch: [],
      ifSearch: false,
      treeData: [],
      defaultProps: {
        children: 'children',
        label: 'deptName',
        icon: 'icon',
        svgIcon: 'svgIcon',
        isLeaf: 'leaf',
      },
      currentNode: {},
    }
  },
  methods: {
    // 初始化异步树
    loadNode(node, resolve) {
      switch (node.level) {
        case 0:
          this.loadFirstLevel(resolve)
          break
        // 加载下级目录
        default:
          this.loadNextLevel(node.data, resolve)
          break
      }
    },
    async loadFirstLevel() {
      const { data } = await queryChildDept({
        parentIndexCode: '0',
      })
      if (data) {
        data.map(ele => {
          ele.icon = 'h-icon-info_organization'
          return ele
        })
        this.treeData = data
        this.currentNode = data[0]
      }
    },
    async loadNextLevel(node, resolve) {
      const { data } = await queryChildDept({
        parentIndexCode: node.deptIndexCode,
      })
      if (data) {
        if (data.length > 0) {
          data.map(ele => {
            ele.icon = 'h-icon-info_organization'
            return ele
          })
        }
        // if (this.ifShowCheckbox) {
        //   // 根据部门编码查找部门所属人员
        //   const result = await queryPerson({
        //     deptIndexCode: node.deptIndexCode,
        //   })
        //   result &&
        //     result.data.forEach(item => {
        //       data.push({
        //         deptIndexCode: item.userIndexCode || item.cameraIndexCode,
        //         deptName: item.userName || item.cameraName,
        //         icon: 'h-icon-user',
        //         leaf: true,
        //         parentIndexCode: node.deptIndexCode,
        //         type: 'user',
        //       })
        //     })
        // }
        return resolve(data)
      }
    },
    async handleInputClick() {
      if (this.inputValue) {
        this.ifSearch = true
        this.$emit('getChckedRegion', [])
        const { data } = await deptqueryTree({
          key: this.inputValue,
        })
        if (data) {
          this.treeDataSearch = data
        }
      } else {
        this.ifSearch = false
      }
    },
    clearIconClick() {
      this.ifSearch = false
    },
    currentChange(data, node) {
      this.currentNode = data
      this.$emit('getRegion', [data])
    },
    handleCheckChange(data, checked, indeterminate) {
      this.$emit('getRegion', this.$refs.simpleTree.getCheckedNodes())
    },
    checkChange(checkedNodes, checkedKeys) {
      this.$emit('getChckedRegion', checkedNodes, checkedKeys)
    },
  },
}
</script>
<style lang="scss">
.el-tree-scrollbar__wrap.el-scrollbar__wrap {
  padding: 1% 5%;
}
</style>
