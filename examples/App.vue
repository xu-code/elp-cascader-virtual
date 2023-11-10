<template>
  <div id="app">
    <cascader :props="props" v-model="values" :options="options" size="small" collapse-tags filterable clearable style="width: 400px"
              :emptyText="emptyText" />
    <!--    <cascader-panel-->
    <!--        :options="options"-->
    <!--        :props="props"-->
    <!--        style="margin: 200px 0"-->
    <!--    />-->
    <!-- <cascader
        v-model="lazyValue"
        :props="lazyMutiProps"
        :options="options"
        style="margin: 100px 0;width: 400px"
        @expand-change="expandChange"
    />
    <cascader
        v-model="lazyCheck"
        :props="lazyMutiProps"
        :options="options"
        :remoteInitMethods="remoteInitMethods"
        style="margin: 100px 0;width: 400px"
        @expand-change="expandChange"
    /> -->

  </div>
</template>

<script>
// import Mock from 'mockjs'
// import ElpCascader from 'elp-cascader/packages'
import ElpCascader from '../packages'
import arr1 from './data.json'
console.log(arr1)
// import { CascaderPanel } from 'element-ui'

const {
  Cascader
  // CascaderPanel
} = ElpCascader

let id = 0

export default {
  name: 'APP',
  components: {
    Cascader
    // CascaderPanel,
  },
  data () {
    console.log('Mock Start')
    console.time('MockStart')
    // const _mock = Mock.mock({
    //   'array|2': [
    //     {
    //       label: '@csentence(6)',
    //       value: '@string()',
    //       'children|5000': [
    //         {
    //           label: '@csentence(6)',
    //           value: '@string()',
    //         }
    //       ]
    //     }
    //   ]
    // })
    // const _singleMock = Mock.mock({
    //   'array|10000': [
    //     {
    //       label: '@csentence(6)',
    //       value: '@string()'
    //     }
    //   ]
    // })
    // console.warn(_singleMock)
    const arr = [
  {
    "recipientType": {
      "first": "USER",
      "second": "用户"
    },
    "children": [
      {
        "first": "Kongxueqin1",
        "second": "孔雪琴1[Kongxueqin1]"
      },
      {
        "first": "Kongxueqin",
        "second": "孔雪琴[Kongxueqin]"
      },
      {
        "first": "Konglaodi",
        "second": "安安[Konglaodi]"
      },
      {
        "first": "Konglaodi1",
        "second": "安安（测试1）[Konglaodi1]"
      },
      {
        "first": "Konglaodi2",
        "second": "安安（测试2）[Konglaodi2]"
      },
      {
        "first": "meng2",
        "second": "张梦2[meng2]"
      },
      {
        "first": "Mandy",
        "second": "张梦[Mandy]"
      },
      {
        "first": "Ponyo",
        "second": "波妞妞[Ponyo]"
      },
      {
        "first": "Ponyo1",
        "second": "波妞（测试1）[Ponyo1]"
      },
      {
        "first": "Ponyo2",
        "second": "波妞（测试2）[Ponyo2]"
      },
      {
        "first": "kkk",
        "second": "3k党头目[kkk]"
      },
      {
        "first": "CCommTrTest2",
        "second": "CCommTrTest2[CCommTrTest2]"
      },
      {
        "first": "CCommTrTest",
        "second": "CCommTrTest[CCommTrTest]"
      },
      {
        "first": "CI",
        "second": "CI测试[CI]"
      },
      {
        "first": "CPackTrTest2",
        "second": "CPackTrTest2[CPackTrTest2]"
      },
      {
        "first": "CPackTrTest",
        "second": "CPackTrTest[CPackTrTest]"
      },
      {
        "first": "ads",
        "second": "ads[ads]"
      },
      {
        "first": "baiyi",
        "second": "baiyi[baiyi]"
      },
      {
        "first": "calebxu",
        "second": "calebxu[calebxu]"
      },
      {
        "first": "cflow",
        "second": "cflow[cflow]"
      },
      {
        "first": "chb-e",
        "second": "chb邮箱[chb-e]"
      },
      {
        "first": "chenhao",
        "second": "chenhao[chenhao]"
      },
      {
        "first": "cjf",
        "second": "cjf1[cjf]"
      },
      {
        "first": "chenjf",
        "second": "cjf[chenjf]"
      },
      {
        "first": "dsy1",
        "second": "dsy1[dsy1]"
      },
      {
        "first": "ericwu",
        "second": "ericwu[ericwu]"
      },
      {
        "first": "ginnymo1",
        "second": "ginnymo1[ginnymo1]"
      },
      {
        "first": "guotao",
        "second": "guotao[guotao]"
      },
      {
        "first": "kooo",
        "second": "gyy[kooo]"
      },
      {
        "first": "halley",
        "second": "halley[halley]"
      },
      {
        "first": "liuzijian",
        "second": "liuzijian[liuzijian]"
      },
      {
        "first": "perreyzhang",
        "second": "perreyzhang[perreyzhang]"
      },
      {
        "first": "ptzhong",
        "second": "ptzhong[ptzhong]"
      },
      {
        "first": "tatsu",
        "second": "tatsu中文名[tatsu]"
      },
      {
        "first": "test10000",
        "second": "test10000[test10000]"
      },
      {
        "first": "test10002",
        "second": "test10002[test10002]"
      },
      {
        "first": "test10004",
        "second": "test10004[test10004]"
      },
      {
        "first": "test10006",
        "second": "test10006[test10006]"
      },
      {
        "first": "test10008",
        "second": "test10008[test10008]"
      },
      {
        "first": "test1000",
        "second": "test1000[test1000]"
      },
      {
        "first": "test10010",
        "second": "test10010[test10010]"
      },
      {
        "first": "test10012",
        "second": "test10012[test10012]"
      },
      {
        "first": "test10014",
        "second": "test10014[test10014]"
      },
      {
        "first": "test10016",
        "second": "test10016[test10016]"
      },
      {
        "first": "test10018",
        "second": "test10018[test10018]"
      },
      {
        "first": "test10020",
        "second": "test10020[test10020]"
      },
      {
        "first": "test10022",
        "second": "test10022[test10022]"
      },
      {
        "first": "test10024",
        "second": "test10024[test10024]"
      },
      {
        "first": "test10026",
        "second": "test10026[test10026]"
      },
      {
        "first": "test10028",
        "second": "test10028[test10028]"
      },
      {
        "first": "test1002",
        "second": "test1002[test1002]"
      },
      {
        "first": "test10030",
        "second": "test10030[test10030]"
      },
      {
        "first": "test10032",
        "second": "test10032[test10032]"
      },
      {
        "first": "test10034",
        "second": "test10034[test10034]"
      },
      {
        "first": "test10036",
        "second": "test10036[test10036]"
      },
      {
        "first": "test10038",
        "second": "test10038[test10038]"
      },
      {
        "first": "test10040",
        "second": "test10040[test10040]"
      },
      {
        "first": "test10042",
        "second": "test10042[test10042]"
      },
      {
        "first": "test10044",
        "second": "test10044[test10044]"
      },
      {
        "first": "test10046",
        "second": "test10046[test10046]"
      },
      {
        "first": "test10048",
        "second": "test10048[test10048]"
      },
      {
        "first": "test1004",
        "second": "test1004[test1004]"
      },
      {
        "first": "test10050",
        "second": "test10050[test10050]"
      },
      {
        "first": "test10051",
        "second": "test10051[test10051]"
      },
      {
        "first": "test10054",
        "second": "test10054[test10054]"
      },
      {
        "first": "test10056",
        "second": "test10056[test10056]"
      },
      {
        "first": "test10058",
        "second": "test10058[test10058]"
      },
      {
        "first": "test10060",
        "second": "test10060[test10060]"
      },
      
      {
        "first": "test10528",
        "second": "test10528[test10528]"
      },
      {
        "first": "test1052",
        "second": "test1052[test1052]"
      },
      {
        "first": "test10530",
        "second": "test10530[test10530]"
      },
      {
        "first": "test10532",
        "second": "test10532[test10532]"
      },
      {
        "first": "test10534",
        "second": "test10534[test10534]"
      },
      {
        "first": "test10536",
        "second": "test10536[test10536]"
      },
      {
        "first": "test10538",
        "second": "test10538[test10538]"
      },
      {
        "first": "test10540",
        "second": "test10540[test10540]"
      },
      {
        "first": "test10542",
        "second": "test10542[test10542]"
      },
      {
        "first": "test10544",
        "second": "test10544[test10544]"
      },
      {
        "first": "test10546",
        "second": "test10546[test10546]"
      },
      {
        "first": "test10548",
        "second": "test10548[test10548]"
      },
      {
        "first": "test1054",
        "second": "test1054[test1054]"
      },
      {
        "first": "test10550",
        "second": "test10550[test10550]"
      },
      {
        "first": "test10552",
        "second": "test10552[test10552]"
      },
      {
        "first": "test10554",
        "second": "test10554[test10554]"
      },
      {
        "first": "test10556",
        "second": "test10556[test10556]"
      },
      {
        "first": "test10557",
        "second": "test10557[test10557]"
      },
      {
        "first": "test10560",
        "second": "test10560[test10560]"
      },
      {
        "first": "test10562",
        "second": "test10562[test10562]"
      },
      {
        "first": "test10564",
        "second": "test10564[test10564]"
      },
      {
        "first": "test10566",
        "second": "test10566[test10566]"
      },
      {
        "first": "test10568",
        "second": "test10568[test10568]"
      },
      {
        "first": "test1056",
        "second": "test1056[test1056]"
      },
      {
        "first": "test10570",
        "second": "test10570[test10570]"
      },
      {
        "first": "test10572",
        "second": "test10572[test10572]"
      },
      {
        "first": "test10574",
        "second": "test10574[test10574]"
      },
      {
        "first": "test10576",
        "second": "test10576[test10576]"
      },
      {
        "first": "test10578",
        "second": "test10578[test10578]"
      },
      {
        "first": "test10580",
        "second": "test10580[test10580]"
      },
      {
        "first": "test10582",
        "second": "test10582[test10582]"
      },
      {
        "first": "test10584",
        "second": "test10584[test10584]"
      },
      {
        "first": "test10586",
        "second": "test10586[test10586]"
      },
      {
        "first": "test10588",
        "second": "test10588[test10588]"
      },
      {
        "first": "test1058",
        "second": "test1058[test1058]"
      },
      {
        "first": "test10590",
        "second": "test10590[test10590]"
      },
      {
        "first": "test10592",
        "second": "test10592[test10592]"
      },
      {
        "first": "test10594",
        "second": "test10594[test10594]"
      },
      {
        "first": "test10596",
        "second": "test10596[test10596]"
      },
      {
        "first": "test10598",
        "second": "test10598[test10598]"
      },
      {
        "first": "test1059",
        "second": "test1059[test1059]"
      },
      {
        "first": "test10600",
        "second": "test10600[test10600]"
      },
      {
        "first": "test10602",
        "second": "test10602[test10602]"
      },
      {
        "first": "test10604",
        "second": "test10604[test10604]"
      },
      {
        "first": "test10606",
        "second": "test10606[test10606]"
      },
      {
        "first": "test10608",
        "second": "test10608[test10608]"
      },
      {
        "first": "test10610",
        "second": "test10610[test10610]"
      },
      {
        "first": "test10612",
        "second": "test10612[test10612]"
      },
      {
        "first": "test10614",
        "second": "test10614[test10614]"
      },
      {
        "first": "test10616",
        "second": "test10616[test10616]"
      },
      {
        "first": "test10618",
        "second": "test10618[test10618]"
      },
      {
        "first": "test10620",
        "second": "test10620[test10620]"
      },
      {
        "first": "test10622",
        "second": "test10622[test10622]"
      },
      {
        "first": "test10624",
        "second": "test10624[test10624]"
      },
      {
        "first": "test10628",
        "second": "test10628[test10628]"
      },
      {
        "first": "test1062",
        "second": "test1062[test1062]"
      },
      {
        "first": "test10630",
        "second": "test10630[test10630]"
      },
      {
        "first": "test10632",
        "second": "test10632[test10632]"
      },
      {
        "first": "test10634",
        "second": "test10634[test10634]"
      },
      {
        "first": "test10636",
        "second": "test10636[test10636]"
      },
      {
        "first": "test10638",
        "second": "test10638[test10638]"
      },
      {
        "first": "test1063",
        "second": "test1063[test1063]"
      },
      {
        "first": "test10640",
        "second": "test10640[test10640]"
      },
      {
        "first": "test10642",
        "second": "test10642[test10642]"
      },
      {
        "first": "test10644",
        "second": "test10644[test10644]"
      },
      {
        "first": "test10648",
        "second": "test10648[test10648]"
      },
      {
        "first": "test10650",
        "second": "test10650[test10650]"
      },
      {
        "first": "test10652",
        "second": "test10652[test10652]"
      },
      {
        "first": "test10654",
        "second": "test10654[test10654]"
      },
      {
        "first": "test10656",
        "second": "test10656[test10656]"
      },
      {
        "first": "test10658",
        "second": "test10658[test10658]"
      },
      {
        "first": "test10660",
        "second": "test10660[test10660]"
      },
      {
        "first": "test10662",
        "second": "test10662[test10662]"
      },
      {
        "first": "test10664",
        "second": "test10664[test10664]"
      },
      {
        "first": "test10666",
        "second": "test10666[test10666]"
      },
      {
        "first": "test10668",
        "second": "test10668[test10668]"
      },
      {
        "first": "test1066",
        "second": "test1066[test1066]"
      },
      {
        "first": "test10670",
        "second": "test10670[test10670]"
      },
      {
        "first": "test10672",
        "second": "test10672[test10672]"
      },
      {
        "first": "test10674",
        "second": "test10674[test10674]"
      },
      {
        "first": "test10676",
        "second": "test10676[test10676]"
      },
      {
        "first": "test10678",
        "second": "test10678[test10678]"
      },
      {
        "first": "test10680",
        "second": "test10680[test10680]"
      },
      {
        "first": "test10682",
        "second": "test10682[test10682]"
      },
      {
        "first": "test10684",
        "second": "test10684[test10684]"
      },
      {
        "first": "test10686",
        "second": "test10686[test10686]"
      },
      {
        "first": "test10688",
        "second": "test10688[test10688]"
      },
      {
        "first": "test1068",
        "second": "test1068[test1068]"
      },
      {
        "first": "test10690",
        "second": "test10690[test10690]"
      },
      {
        "first": "test10692",
        "second": "test10692[test10692]"
      },
      
      {
        "first": "tonychen",
        "second": "tonychen[tonychen]"
      },
      {
        "first": "xiaoshanwen",
        "second": "xiaoshanwen[xiaoshanwen]"
      },
      {
        "first": "xudh",
        "second": "xudh[xudh]"
      },
      {
        "first": "xuhong",
        "second": "xuhong[xuhong]"
      },
      {
        "first": "xujian",
        "second": "xujian[xujian]"
      },
      {
        "first": "yuan1",
        "second": "yuan1[yuan1]"
      },
      {
        "first": "yuan",
        "second": "yuan[yuan]"
      },
      {
        "first": "zcb2",
        "second": "zcb2[zcb2]"
      },
      {
        "first": "zcb",
        "second": "zcb[zcb]"
      },
      {
        "first": "ZJ",
        "second": "zhangjiang[ZJ]"
      },
      {
        "first": "jackzou",
        "second": "zs[jackzou]"
      },
      {
        "first": "heqi",
        "second": "何琦[heqi]"
      },
      {
        "first": "ericxuan",
        "second": "你相信光吗？[ericxuan]"
      },
      {
        "first": "dawn",
        "second": "侯剑华[dawn]"
      },
      {
        "first": "chb1",
        "second": "斌-新[chb1]"
      },
      {
        "first": "chb",
        "second": "斌[chb]"
      },
      {
        "first": "jackfang",
        "second": "方亮[jackfang]"
      },
      {
        "first": "gjq",
        "second": "本故事纯属虚构[gjq]"
      },
      {
        "first": "locals",
        "second": "李伟剑[locals]"
      },
      {
        "first": "harrison",
        "second": "李昊政[harrison]"
      },
      {
        "first": "ljz",
        "second": "梁家彰[ljz]"
      },
      {
        "first": "xiaoyushen",
        "second": "沈小瑜[xiaoyushen]"
      },
      {
        "first": "Osian",
        "second": "法外狂徒张三[Osian]"
      },
      {
        "first": "sxwxw",
        "second": "王祥文[sxwxw]"
      },
      {
        "first": "yhjy",
        "second": "用户禁用[yhjy]"
      },
      {
        "first": "ginnymo",
        "second": "磨金妮[ginnymo]"
      },
      {
        "first": "zhgly",
        "second": "租户管理员[zhgly]"
      },
      {
        "first": "fzh",
        "second": "范志辉1[fzh]"
      },
      {
        "first": "ps1",
        "second": "评审用户1[ps1]"
      },
      {
        "first": "ps2",
        "second": "评审用户2[ps2]"
      },
      {
        "first": "ps3",
        "second": "评审用户3[ps3]"
      },
      {
        "first": "cjgly",
        "second": "超级管理员[cjgly]"
      },
      {
        "first": "dsy",
        "second": "邓时雨[dsy]"
      },
      {
        "first": "sx_qiupeizhi",
        "second": "邱佩芝[sx_qiupeizhi]"
      },
      {
        "first": "alisazou",
        "second": "邹嘉靖[alisazou]"
      }
    ]
  },
  {
    "recipientType": {
      "first": "ROLES",
      "second": "角色"
    },
    "children": [
      {
        "first": "200000000000002",
        "second": "开发人员"
      },
      {
        "first": "200000000000010",
        "second": "开发管理员"
      },
      {
        "first": "200000000000003",
        "second": "测试人员"
      },
      {
        "first": "200000000000008",
        "second": "测试管理员"
      },
      {
        "first": "200000000000004",
        "second": "运维人员"
      },
      {
        "first": "200000000000001",
        "second": "需求人员"
      },
      {
        "first": "200000000000009",
        "second": "需求管理员"
      },
      {
        "first": "a5653eab57ea42049fa185f8964785a6",
        "second": "项目内添加的角色"
      }
    ]
  },
  {
    "recipientType": {
      "first": "USER_FIELD",
      "second": "指定字段"
    },
    "children": [
      {
        "first": "operator_user",
        "second": "经办人"
      },
      {
        "first": "propose_user",
        "second": "提出人"
      }
    ]
  }
].map(item => {
  return {
    first:item.recipientType.first,
    second: item.recipientType.second,
    children: item.children
  }
})
const values = arr1[0].children.map(item => {
  return [arr[0].first, item.first]
})
arr[0].children = [...arr[0].children,...arr[0].children,]
arr[0].children = [...arr[0].children,...arr[0].children,]
arr[0].children = [...arr[0].children,...arr[0].children,]
arr[0].children = [...arr[0].children,...arr[0].children,]
arr[0].children = [...arr[0].children,...arr[0].children,]
arr[0].children = [...arr[0].children,...arr[0].children,]
arr[0].children = [...arr[0].children,...arr[0].children,]
console.log(arr)
const arr2 = arr1.map(item => {
  return {
    first:item.recipientType.first,
    second: item.recipientType.second,
    children: item.children
  }
})
    console.timeEnd('MockStart')
    return {
      values,
      value: [],
      // options: [],
      options: arr2,
      props: {
        value: 'first',
        label: 'second',
        children: 'children',
        multiple: true,
        checkStrictly: false,
        selectWithExpand: false,
        panelSearch: true,
        panelLabels: ['一级类目', '二级类目', '三级类目'],
        panelPlaceholder: ['请搜索一级', '请搜索二级', '请搜索三级'],
        // lazy: true,
        // lazyLoad (node, resolve) {
        //   // const { level } = node
        //   setTimeout(() => {
        //     resolve(_singleMock)
        //   }, 1000)
        // }
        // expandTrigger: 'hover'
      },
      emptyText: 'no data',
      // lazy cascader
      lazyValue: [
        ['1', '2']
      ],
      lazyCheck: [],
      lazyOptions: [
        // { label: '111', value: '111', children: [] },
        // { label: '选项1', value: '1', children: [{ label: '选项2', value: '2' }] }
      ],
      lazyProps: {
        lazy: true,
        multiple: true,
        checkStrictly: false,
        lazyMultiCheck: true,
        panelLabels: ['一级类目', '二级类目', '三级类目'],
        lazyLoad (node, resolve) {
          const { level } = node
          setTimeout(() => {
            const nodes = Array.from({ length: level + 1 }).map(() => ({
              value: String(++id),
              label: `选项${id}`,
              leaf: level >= 3
            }))
            // 通过调用resolve将子节点数据返回，通知组件数据加载完成
            resolve(nodes)
          }, 1000)
        }
      },
      lazyMutiProps: {
        lazy: true,
        multiple: true,
        checkStrictly: true,
        panelSearch: true,
        checkAll: true,
        panelLabels: ['数据连接', '分类', '数据源'],
        panelPlaceholder: ['远程搜素'],
        lazyLoad (node, resolve) {
          const { level } = node
          setTimeout(() => {
            const nodes = Array.from({ length: level + 1 }).map(() => ({
              value: String(++id),
              label: `选项${id}`,
              // disabled: true,
              leaf: level >= 3
            }))
            // 通过调用resolve将子节点数据返回，通知组件数据加载完成
            resolve(nodes)
          }, 1000)
        }
      }
    }
  },
  methods: {
    expandChange (parentArr) {
      console.info(parentArr)
    },
    remoteInitMethods (key, resolve) {
      setTimeout(() => {
        resolve([ {label: 1, value: 1}, {label: 2, value: 2}])
      }, 500)
    }
  }
}
</script>

<style>
#app {
  display: grid;
  place-items: flex-start;
  margin: 60px;
}
</style>

