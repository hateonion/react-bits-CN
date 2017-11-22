# Handling UX variations for multiple brands and apps


## [Vasa做的关于react组件复用的演讲](https://speakerdeck.com/vasa/building-multitenant-ui-with-react-dot-js)


以下是一些有助于编写高复用性react组件的通用编码原则。

## 单功能原则

**使用react时**

组件或容器的代码在根本上必须只负责一块UI功能。

* 以设计收货地址组件为例

* 收货地址组件可以拆分为地址组件（只含有地址相关内容），姓名组件（包括姓氏和名字），电话组件，省，市和邮政编码组件。

**使用redux时**

All API related call go into Redux thunks/other async handling sections (redux-promise, sagas etc)所有API相关操作可以使用redux或者其他异步模块（如redux-promise, sagas等）来处理。模块可以如下划分：

* 一些模块只负责在AJAX请求成功或失败的时候派发动作。

* 一些模块通过promise来接收。

## 让组件保持简单 (KISS)

* 如果组件根本不需要状态，那么就使用函数定义的无状态组件。

* 从性能上来说，**函数定义的无状态组件 > ES6 class 定义的组件 > 通过React.createClass()定义的组件**。

* 仅传递组件所需要的属性。只有当属性列表太长时，才使用{...this.props}进行传递。

* 如果组件里面有太多的判断逻辑（if-else语句）通常意味着这个组件需要被拆分成更细的组件或模块。

* 还有一点，使用明确的命名能够让开发者明白它的功能，有助于组件复用。

## 相关文章

[Building React Components for Multiple Brands and Applications](https://medium.com/walmartlabs/building-react-components-for-multiple-brands-and-applications-7e9157a39db4)

