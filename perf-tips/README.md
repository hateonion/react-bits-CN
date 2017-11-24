# Perf Tips

**基本准则**

- 在`shouldComponentUpdate`中避免不必要的检查.

- 使用不可变数据类型(Immutable).

- 编写针对产品环境的打包配置(Production Build).

- 通过Chrome Timeline来记录组件所耗费的资源.

- 在`componentWillMount`或者`componentDidMount`里面通过`setTimeOut`或者`requestAnimationFram`来延迟执行那些需要大量计算的任务. 

## 相关文章

[Optimizing Performance: Docs](https://facebook.github.io/react/docs/optimizing-performance.html)

[Performance Engineering with React](http://benchling.engineering/performance-engineering-with-react/)

[Tips to optimise rendering of a set of elements in React](https://blog.lavrton.com/how-to-optimise-rendering-of-a-set-of-elements-in-react-ad01f5b161ae)

[React.js Best Practices for 2016](https://blog.risingstack.com/react-js-best-practices-for-2016/)
