<template>
  <a-layout id="components-layout-demo-top" class="layout">
    <a-layout-header>
      <a-menu theme="dark" mode="horizontal" :defaultSelectedKeys="['2']" :style="{ lineHeight: '64px' }">
        <a-menu-item key="1">nav 1</a-menu-item>
        <a-menu-item key="2">nav 2</a-menu-item>
        <a-menu-item key="3">nav 3</a-menu-item>
      </a-menu>
    </a-layout-header>
    <a-layout-content style="padding: 0 50px">
      <div :style="{ background: '#fff', padding: '24px', minHeight: '480px' }">
        <a-space direction="vertical" :size="size">
          <!-- 选择组件尺寸 -->
          <a-space>
            <a-radio-group v-model="size">
              组件尺寸：
              <a-radio value="small">小</a-radio>
              <a-radio value="middle">正常</a-radio>
              <a-radio value="large">大</a-radio>
            </a-radio-group>
          </a-space>
          <!-- 按钮组件 -->
          <a-space>
            按钮组件：
            <a-button type="primary" :size="size">
              主按钮
            </a-button>
            <a-button :size="size">
              次按钮
            </a-button>
            <a-button :size="size">
              辅助按钮
            </a-button>
            <a-dropdown>
              <a-menu slot="overlay">
                <a-menu-item key="1">
                  按钮一
                </a-menu-item>
                <a-menu-item key="2">
                  按钮二
                </a-menu-item>
                <a-menu-item key="3">
                  按钮三
                </a-menu-item>
              </a-menu>
              <a-button :size="size">
                下拉按钮
                <icon-font type="iconxia" />
              </a-button>
            </a-dropdown>
            <a-button-group>
              <a-button :size="size" disabled>
                按钮一
              </a-button>
              <a-button :size="size">
                按钮二
              </a-button>
              <a-button :size="size">
                按钮三
              </a-button>
            </a-button-group>
            <a-button type="link" :size="size">
              链接
            </a-button>
          </a-space>
          <a-space>
            <!-- 图标组件 -->
            图标组件：
            <icon-font type="iconshezhi" />
            <a-button :size="size">
              <icon-font type="iconshezhi" />
            </a-button>
            <a-button :size="size">
              <icon-font type="iconshezhi" />
              图标按钮
            </a-button>
          </a-space>
          <!-- 面包屑组件 -->
          <a-space>
            面包屑组件：
            <a-breadcrumb>
              <a-breadcrumb-item>首页</a-breadcrumb-item>
              <a-breadcrumb-item>
                <a href="">层级标题</a>
              </a-breadcrumb-item>
              <a-breadcrumb-item>
                <a href="">层级标题</a>
              </a-breadcrumb-item>
              <a-breadcrumb-item>页面当前标题</a-breadcrumb-item>
            </a-breadcrumb>
            <a-breadcrumb>
              <a-breadcrumb-item href="">
                <icon-font type="icongongzuotai" />
              </a-breadcrumb-item>
              <a-breadcrumb-item href="">
                <icon-font type="icongeren" />
                <span>层级标题</span>
              </a-breadcrumb-item>
              <a-breadcrumb-item>
                页面当前标题
              </a-breadcrumb-item>
            </a-breadcrumb>
            <a-breadcrumb>
              <a-breadcrumb-item>首页</a-breadcrumb-item>
              <a-breadcrumb-item><a href="">层级标题</a></a-breadcrumb-item>
              <a-breadcrumb-item>
                <a href="">层级标题</a>
                <a-menu slot="overlay">
                  <a-menu-item>
                    <a target="_blank">
                      子标题一
                    </a>
                  </a-menu-item>
                  <a-menu-item>
                    <a target="_blank">
                      子标题二
                    </a>
                  </a-menu-item>
                  <a-menu-item>
                    <a target="_blank">
                      子标题三
                    </a>
                  </a-menu-item>
                </a-menu>
              </a-breadcrumb-item>
              <a-breadcrumb-item>页面当前标题</a-breadcrumb-item>
            </a-breadcrumb>
          </a-space>
          <!-- 下拉菜单组件 -->
          <a-space>
            下拉菜单组件：
            <a-dropdown :size="size">
              <a class="ant-dropdown-link">
                更多
              </a>
              <a-menu slot="overlay">
                <a-menu-item>
                  <a>导出</a>
                </a-menu-item>
                <a-menu-item>
                  <a href="">刷新</a>
                </a-menu-item>
                <a-menu-item>
                  <a href="">全屏（鼠标经过）</a>
                </a-menu-item>
              </a-menu>
            </a-dropdown>
            下拉菜单：
            <a-select default-value="1" style="width: 120px">
              <icon-font slot="suffixIcon" type="iconxia" />
              <a-select-option value="1">
                Jack
              </a-select-option>
              <a-select-option value="2">
                Lucy
              </a-select-option>
              <a-select-option value="3" disabled>
                Disabled
              </a-select-option>
              <a-select-option value="4">
                yiminghe
              </a-select-option>
            </a-select>
          </a-space>
          <!-- 分页组件 -->
          <a-space>
            分页组件：
            <a-pagination show-quick-jumper :default-current="2" :total="500" @change="onChange" />
          </a-space>
          <a-space>
            <a-pagination show-quick-jumper :default-current="2" :total="500" disabled show-less-items
              @change="onChange" />
          </a-space>
          <!-- 步骤条组件 -->
          <a-space>
            步骤条组件：
            <a-steps :current="1">
              <a-step>
                <!-- <span slot="title">Finished</span> -->
                <template slot="title">
                  Finished
                </template>
                <span slot="description">This is a description.</span>
              </a-step>
              <a-step title="In Progress" description="This is a description." />
              <a-step title="Waiting" description="This is a description." />
            </a-steps>
            <a-steps direction="vertical" :current="1">
              <a-step title="Finished" description="This is a description." />
              <a-step title="In Progress" description="This is a description." />
              <a-step title="Waiting" description="This is a description." />
            </a-steps>
          </a-space>
          <!-- 多选组件 -->
          <a-space>
            多选组件：
            <a-checkbox-group>
              <a-row>
                <a-col :span="8">
                  <a-checkbox value="A">
                    A
                  </a-checkbox>
                </a-col>
                <a-col :span="8">
                  <a-checkbox value="B">
                    B
                  </a-checkbox>
                </a-col>
                <a-col :span="8">
                  <a-checkbox value="C">
                    C
                  </a-checkbox>
                </a-col>
                <a-col :span="8">
                  <a-checkbox value="D">
                    D
                  </a-checkbox>
                </a-col>
                <a-col :span="8">
                  <a-checkbox value="E">
                    E
                  </a-checkbox>
                </a-col>
              </a-row>
            </a-checkbox-group>
          </a-space>
          <!-- 级联选择组件 -->
          <a-space>
            级联选择组件：
            <a-cascader :options="options" placeholder="Please select" />
          </a-space>
          <!-- 日期选择组件 -->
          <a-space>
            日期选择组件：
            <a-date-picker />
            <a-range-picker />
          </a-space>
          <!-- 表单组件 -->
          <a-space>
            表单组件：
            <a-form :form="form" :label-col="{ span: 5 }" :wrapper-col="{ span: 12 }" @submit="handleSubmit">
              <a-form-item label="Note">
                <a-input v-decorator="['note', { rules: [{ required: true, message: 'Please input your note!' }] }]" />
              </a-form-item>
              <a-form-item label="Gender">
                <a-select v-decorator="[
                    'gender',
                    { rules: [{ required: true, message: 'Please select your gender!' }] },
                  ]" placeholder="Select a option and change input text above" @change="handleSelectChange">
                  <a-select-option value="male">
                    male
                  </a-select-option>
                  <a-select-option value="female">
                    female
                  </a-select-option>
                </a-select>
              </a-form-item>
              <a-form-item :wrapper-col="{ span: 12, offset: 5 }">
                <a-button type="primary" html-type="submit">
                  Submit
                </a-button>
              </a-form-item>
            </a-form>
          </a-space>
          <!-- 开关组件 -->
          <a-space>
            开关组件：
            <a-switch default-checked />
          </a-space>
        </a-space>
      </div>
    </a-layout-content>
    <a-layout-footer style="text-align: center">
      Ant Design Vue ©2020 Created by 董天宇
    </a-layout-footer>
  </a-layout>
</template>

<script>
  import {
    Icon
  } from "ant-design-vue";

  const IconFont = Icon.createFromIconfontCN({
    scriptUrl: "//at.alicdn.com/t/font_1389343_piwa5v5qoj.js"
  });
  export default {
    components: {
      IconFont
    },
    data() {
      return {
        size: "middle",
        options: [{
            value: 'zhejiang',
            label: 'Zhejiang',
            children: [{
              value: 'hangzhou',
              label: 'Hangzhou',
              children: [{
                value: 'xihu',
                label: 'West Lake',
              }, ],
            }, ],
          },
          {
            value: 'jiangsu',
            label: 'Jiangsu',
            children: [{
              value: 'nanjing',
              label: 'Nanjing',
              children: [{
                value: 'zhonghuamen',
                label: 'Zhong Hua Men',
              }, ],
            }, ],
          },
        ],
      };
    },
    methods: {}
  };
</script>