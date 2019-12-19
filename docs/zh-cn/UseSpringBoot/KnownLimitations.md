<h2>8.2.7 已知局限性</h2>

重新启动功能不适用于通过使用标准反序列化的对象```ObjectInputStream```。如果你需要对数据进行反序列化，你可能需要使用Spring的```ConfigurableObjectInputStream```结合```Thread.currentThread().getContextClassLoader()```。

不幸的是，一些第三方库在反序列化时没有考虑上下文类加载器的情况。如果发现这样的问题，则需要向原始作者请求修复。
