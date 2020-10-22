<template>
  <a-layout id="components-layout-demo-top" class="layout">
    <a-layout-header>
      <a-menu theme="dark" mode="horizontal" :defaultSelectedKeys="['2']"
        style=" text-align: center; line-height: 64px">
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
            <a-pagination show-quick-jumper :default-current="2" :total="500" />
          </a-space>
          <a-space>
            <a-pagination show-quick-jumper :default-current="2" :total="500" disabled show-less-items />
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
                <a-input v-decorator="[
                    'note',
                    {
                      rules: [
                        { required: true, message: 'Please input your note!' }
                      ]
                    }
                  ]" />
              </a-form-item>
              <a-form-item label="Gender">
                <a-select v-decorator="[
                    'gender',
                    {
                      rules: [
                        {
                          required: true,
                          message: 'Please select your gender!'
                        }
                      ]
                    }
                  ]" placeholder="Select a option and change input text above">
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
          <!-- 树选择组件 -->
          <a-space>
            树选择组件:
            <a-tree-select v-model="value" show-search style="width: 200px"
              :dropdown-style="{ maxHeight: '400px', overflow: 'auto' }" placeholder="Please select" allow-clear
              tree-default-expand-all>
              <a-tree-select-node key="0-1" value="parent 1" title="parent 1">
                <a-tree-select-node key="0-1-1" value="parent 1-0" title="parent 1-0">
                  <a-tree-select-node key="random" :selectable="false" value="leaf1" title="my leaf" />
                  <a-tree-select-node key="random1" value="leaf2" title="your leaf" />
                </a-tree-select-node>
                <a-tree-select-node key="random2" value="parent 1-1" title="parent 1-1">
                  <a-tree-select-node key="random3" value="sss">
                    <b slot="title" style="color: #08c">sss</b>
                  </a-tree-select-node>
                </a-tree-select-node>
              </a-tree-select-node>
            </a-tree-select>
          </a-space>
          <!-- 穿梭框组件 -->
          <a-sapce>
            穿梭框组件:
            <a-transfer :data-source="mockData" :titles="['Source', 'Target']" :target-keys="targetKeys"
              :selected-keys="selectedKeys" :render="item => item.title" :disabled="disabled"
              @selectChange="handleSelectChange" @scroll="handleScroll" />
            <a-switch un-checked-children="enabled" checked-children="disabled" :checked="disabled"
              style="margin-top: 16px" />
          </a-sapce>
          <!-- 折叠面板组件 -->
          <a-space>
            折叠面板组件:
            <a-collapse default-active-key="1">
              <a-collapse-panel key="1" header="This is panel header with arrow icon">
                <p>{{ text }}</p>
              </a-collapse-panel>
              <a-collapse-panel key="2" header="This is panel header with no arrow icon" :show-arrow="false">
                <p>{{ text }}</p>
              </a-collapse-panel>
            </a-collapse>
          </a-space>
          <!-- 卡片组件 -->
          <a-space>
            卡片组件：
            <a-card title="卡片组件" hoverable style="width: 300px">
              <a slot="extra" href="#">more</a>
              <p>card content</p>
              <p>card content</p>
              <p>card content</p>
            </a-card>
          </a-space>
          <!-- 描述列表组件 -->
          <a-space>
            描述列表组件：
            <a-descriptions title="描述列表组件" bordered>
              <a-descriptions-item label="UserName">
                Zhou Maomao
              </a-descriptions-item>
              <a-descriptions-item label="Telephone">
                1810000000
              </a-descriptions-item>
              <a-descriptions-item label="Live">
                Hangzhou, Zhejiang
              </a-descriptions-item>
              <a-descriptions-item label="Remark">
                empty
              </a-descriptions-item>
              <a-descriptions-item label="Address">
                No. 18, Wantang Road, Xihu District, Hangzhou, Zhejiang, China
              </a-descriptions-item>
            </a-descriptions>
          </a-space>
          <!-- 气泡确认框组件 -->
          <a-space>
            气泡确认框组件：
            <a-popconfirm title="Are you sure delete this task?" ok-text="Yes" cancel-text="No" @confirm="confirm"
              @cancel="cancel">
              <a href="#">Delete</a>
            </a-popconfirm>
          </a-space>
          <!-- 标签组件 -->
          <a-space>
            标签组件：
            <a-tag>Tag 1</a-tag>
            <a-tag><a href="/">Link</a></a-tag>
            <a-tag closable>
              Tag 2
            </a-tag>
            <a-tag closable>
              Prevent Default
            </a-tag>
          </a-space>
          <!-- 警告提示组件 -->
          <a-space>
            警告提示组件：
            <a-alert message="Success Tips" description="Detailed description and advices about successful copywriting."
              type="success" show-icon />
            <a-alert message="Informational Notes"
              description="Additional description and informations about copywriting." type="info" show-icon />
            <a-alert message="Warning" description="This is a warning notice about copywriting." type="warning"
              show-icon />
            <a-alert message="Error" description="This is an error message about copywriting." type="error" show-icon />
          </a-space>
          <!-- 抽屉组件 -->
          <a-space>
            抽屉组件：
            <a-radio-group style="margin-right: 8px" :default-value="placement" @change="onChange">
              <a-radio value="top">
                top
              </a-radio>
              <a-radio value="right">
                right
              </a-radio>
              <a-radio value="bottom">
                bottom
              </a-radio>
              <a-radio value="left">
                left
              </a-radio>
            </a-radio-group>
            <a-button type="primary" @click="showDrawer">
              Open
            </a-button>
            <a-drawer title="Basic Drawer" :placement="placement" :closable="false" :visible="visible" @close="onClose">
              <p>Some contents...</p>
              <p>Some contents...</p>
              <p>Some contents...</p>
            </a-drawer>
          </a-space>
          <!-- 加载中组件 -->
          <a-space>
            加载中组件：
            <a-spin :size="size" />
          </a-space>
          <!-- 通知提醒组件 -->
          <a-space>
            通知提醒组件：
            <a-button @click="() => openNotificationWithIcon('success')">
              Success
            </a-button>
            <a-button @click="() => openNotificationWithIcon('info')">
              Info
            </a-button>
            <a-button @click="() => openNotificationWithIcon('warning')">
              Warning
            </a-button>
            <a-button @click="() => openNotificationWithIcon('error')">
              Error
            </a-button>
          </a-space>
          <!-- 页签组件 -->
          <a-space>
            页签组件：
            <div :style="{ marginBottom: '16px' }">
              <a-button @click="add">
                ADD
              </a-button>
            </div>
            <a-tabs v-model="activeKey" hide-add type="editable-card" @edit="onEdit">
              <a-tab-pane v-for="pane in panes" :key="pane.key" :tab="pane.title" :closable="pane.closable">
                {{ pane.content }}
              </a-tab-pane>
            </a-tabs>
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
      const mockData = [];
      for (let i = 0; i < 20; i++) {
        mockData.push({
          key: i.toString(),
          title: `content${i + 1}`,
          description: `description of content${i + 1}`,
          disabled: i % 3 < 1
        });
      }

      const oriTargetKeys = mockData
        .filter(item => +item.key % 3 > 1)
        .map(item => item.key);
      const panes = [{
          title: 'Tab 1',
          content: 'Content of Tab 1',
          key: '1'
        },
        {
          title: 'Tab 2',
          content: 'Content of Tab 2',
          key: '2'
        },
      ];
      return {
        size: "middle",
        options: [{
            value: "zhejiang",
            label: "Zhejiang",
            children: [{
              value: "hangzhou",
              label: "Hangzhou",
              children: [{
                value: "xihu",
                label: "West Lake"
              }]
            }]
          },
          {
            value: "jiangsu",
            label: "Jiangsu",
            children: [{
              value: "nanjing",
              label: "Nanjing",
              children: [{
                value: "zhonghuamen",
                label: "Zhong Hua Men"
              }]
            }]
          }
        ],
        treeExpandedKeys: [],
        value: undefined,
        mockData,
        targetKeys: oriTargetKeys,
        selectedKeys: ["1", "4"],
        disabled: false,
        text: `20201019 16:55 折叠面板组件`,
        visible: false,
        placement: 'left',
        activeKey: panes[0].key,
        panes,
        newTabIndex: 0,
      };
    },

    methods: {
      handleChange(nextTargetKeys, direction, moveKeys) {
        this.targetKeys = nextTargetKeys;
      },
      handleSelectChange(sourceSelectedKeys, targetSelectedKeys) {
        this.selectedKeys = [...sourceSelectedKeys, ...targetSelectedKeys];
      },
      handleDisable(disabled) {
        this.disabled = disabled;
      },
      confirm(e) {
        this.$message.success('Click on Yes');
      },
      cancel(e) {
        this.$message.error('Click on No');
      },
      showDrawer() {
        this.visible = true;
      },
      onClose() {
        this.visible = false;
      },
      onChange(e) {
        this.placement = e.target.value;
      },
      openNotificationWithIcon(type) {
        this.$notification[type]({
          message: 'Notification Title',
          description: 'This is the content of the notification. This is the content of the notification. This is the content of the notification.',
        });
      },
      onEdit(targetKey, action) {
        this[action](targetKey);
      },
      add() {
        const panes = this.panes;
        const activeKey = `newTab${this.newTabIndex++}`;
        panes.push({
          title: `New Tab ${activeKey}`,
          content: `Content of new Tab ${activeKey}`,
          key: activeKey,
        });
        this.panes = panes;
        this.activeKey = activeKey;
      },
      remove(targetKey) {
        let activeKey = this.activeKey;
        let lastIndex;
        this.panes.forEach((pane, i) => {
          if (pane.key === targetKey) {
            lastIndex = i - 1;
          }
        });
        const panes = this.panes.filter(pane => pane.key !== targetKey);
        if (panes.length && activeKey === targetKey) {
          if (lastIndex >= 0) {
            activeKey = panes[lastIndex].key;
          } else {
            activeKey = panes[0].key;
          }
        }
        this.panes = panes;
        this.activeKey = activeKey;
      },
    }
  };
</script>