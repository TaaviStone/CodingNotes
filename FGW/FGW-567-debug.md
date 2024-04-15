13 13:54:59.394 DEBUG [main] io.netty.channel.DefaultChannelId
                        -Dio.netty.machineId: 00:15:5d:ff:fe:bf:16:8d (auto-detected)
2024-03-13 13:54:59,482 main TRACE Log4jLoggerFactory.getContext() found anchor class io.netty.util.internal.logging.Slf4JLoggerFactory
2024-03-13 13:54:59,614 main TRACE Log4jLoggerFactory.getContext() found anchor class io.netty.util.internal.logging.Slf4JLoggerFactory
2024-03-13 13:54:59,659 main TRACE Log4jLoggerFactory.getContext() found anchor class io.netty.util.internal.logging.Slf4JLoggerFactory
2024-03-13 13:54:59,692 main TRACE Log4jLoggerFactory.getContext() found anchor class io.netty.util.internal.logging.Slf4JLoggerFactory
2024-03-13 13:54:59,892 main TRACE Log4jLoggerFactory.getContext() found anchor class reactor.util.Loggers$Slf4JLoggerFactory
 2024-03-13 13:54:59.893 WARN  [main] reactor.core.Exceptions
                        throwIfFatal detected a jvm fatal exception, which is thrown and logged below:
java.lang.UnsatisfiedLinkError: io.netty.channel.unix.LimitsStaticallyReferencedJniMethods.iovMax()I
        at io.netty.channel.unix.LimitsStaticallyReferencedJniMethods.iovMax(Native Method) ~[netty-transport-native-unix-common-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.unix.Limits.<clinit>(Limits.java:24) ~[netty-transport-native-unix-common-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollChannelConfig.<init>(EpollChannelConfig.java:36) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollSocketChannelConfig.<init>(EpollSocketChannelConfig.java:48) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollSocketChannel.<init>(EpollSocketChannel.java:51) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at reactor.netty.resources.DefaultLoopEpoll.getChannel(DefaultLoopEpoll.java:51) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.LoopResources.onChannel(LoopResources.java:243) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.tcp.TcpResources.onChannel(TcpResources.java:251) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConfig.lambda$connectionFactory$1(TransportConfig.java:266) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.doInitAndRegister(TransportConnector.java:282) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.connect(TransportConnector.java:164) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.connect(TransportConnector.java:123) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.DefaultPooledConnectionProvider$PooledConnectionAllocator.lambda$connectChannel$0(DefaultPooledConnectionProvider.java:519) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4490) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribeWith(Mono.java:4605) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4457) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4393) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.drainLoop(SimpleDequePool.java:437) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.pendingOffer(SimpleDequePool.java:600) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.doAcquire(SimpleDequePool.java:296) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.AbstractPool$Borrower.request(AbstractPool.java:430) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.DefaultPooledConnectionProvider$DisposableAcquire.onSubscribe(DefaultPooledConnectionProvider.java:204) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool$QueueBorrowerMono.subscribe(SimpleDequePool.java:720) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.PooledConnectionProvider.lambda$acquire$2(PooledConnectionProvider.java:170) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.http.client.HttpClientConnect$MonoHttpConnect.lambda$subscribe$0(HttpClientConnect.java:273) ~[reactor-netty-http-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.FluxRetryWhen.subscribe(FluxRetryWhen.java:77) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.MonoRetryWhen.subscribeOrReturn(MonoRetryWhen.java:46) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.InternalMonoOperator.subscribe(InternalMonoOperator.java:57) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.http.client.HttpClientConnect$MonoHttpConnect.subscribe(HttpClientConnect.java:276) ~[reactor-netty-http-1.0.30.jar:1.0.30]
        at reactor.core.publisher.InternalMonoOperator.subscribe(InternalMonoOperator.java:64) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.MonoDefer.subscribe(MonoDefer.java:52) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4490) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.block(Mono.java:1741) ~[reactor-core-3.4.28.jar:3.4.28]
        at lt.dataHandlers.SoapServiceClient.sendRequestAndGetResponse(SoapServiceClient.java:44) ~[test-classes/:?]
        at lt.dataHandlers.SoapServiceClient.sendRequestAndParseResponse(SoapServiceClient.java:20) ~[test-classes/:?]
        at lt.GetServicesLoadTest.<init>(GetServicesLoadTest.java:33) ~[test-classes/:?]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance0(Native Method) ~[?:1.8.0_382]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance(NativeConstructorAccessorImpl.java:62) ~[?:1.8.0_382]
        at sun.reflect.DelegatingConstructorAccessorImpl.newInstance(DelegatingConstructorAccessorImpl.java:45) ~[?:1.8.0_382]
        at java.lang.reflect.Constructor.newInstance(Constructor.java:423) ~[?:1.8.0_382]
        at io.gatling.app.SimulationClass$Java.params(SimulationClass.scala:35) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Runner.load(Runner.scala:72) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Runner.run(Runner.scala:57) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.start(Gatling.scala:89) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.fromArgs(Gatling.scala:51) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.main(Gatling.scala:39) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling.main(Gatling.scala) ~[gatling-app-3.9.5.jar:3.9.5]
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method) ~[?:1.8.0_382]
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62) ~[?:1.8.0_382]
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43) ~[?:1.8.0_382]
        at java.lang.reflect.Method.invoke(Method.java:498) ~[?:1.8.0_382]
        at io.gatling.plugin.util.ForkMain.runMain(ForkMain.java:67) ~[gatling-enterprise-plugin-commons-1.5.1.jar:1.5.1]
        at io.gatling.plugin.util.ForkMain.main(ForkMain.java:35) ~[gatling-enterprise-plugin-commons-1.5.1.jar:1.5.1]
 2024-03-13 13:54:59.927 WARN  [main] reactor.core.Exceptions
                        throwIfFatal detected a jvm fatal exception, which is thrown and logged below:
java.lang.UnsatisfiedLinkError: io.netty.channel.unix.LimitsStaticallyReferencedJniMethods.iovMax()I
        at io.netty.channel.unix.LimitsStaticallyReferencedJniMethods.iovMax(Native Method) ~[netty-transport-native-unix-common-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.unix.Limits.<clinit>(Limits.java:24) ~[netty-transport-native-unix-common-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollChannelConfig.<init>(EpollChannelConfig.java:36) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollSocketChannelConfig.<init>(EpollSocketChannelConfig.java:48) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollSocketChannel.<init>(EpollSocketChannel.java:51) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at reactor.netty.resources.DefaultLoopEpoll.getChannel(DefaultLoopEpoll.java:51) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.LoopResources.onChannel(LoopResources.java:243) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.tcp.TcpResources.onChannel(TcpResources.java:251) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConfig.lambda$connectionFactory$1(TransportConfig.java:266) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.doInitAndRegister(TransportConnector.java:282) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.connect(TransportConnector.java:164) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.connect(TransportConnector.java:123) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.DefaultPooledConnectionProvider$PooledConnectionAllocator.lambda$connectChannel$0(DefaultPooledConnectionProvider.java:519) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4490) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribeWith(Mono.java:4605) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4457) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4393) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.drainLoop(SimpleDequePool.java:437) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.pendingOffer(SimpleDequePool.java:600) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.doAcquire(SimpleDequePool.java:296) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.AbstractPool$Borrower.request(AbstractPool.java:430) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.DefaultPooledConnectionProvider$DisposableAcquire.onSubscribe(DefaultPooledConnectionProvider.java:204) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool$QueueBorrowerMono.subscribe(SimpleDequePool.java:720) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.PooledConnectionProvider.lambda$acquire$2(PooledConnectionProvider.java:170) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.http.client.HttpClientConnect$MonoHttpConnect.lambda$subscribe$0(HttpClientConnect.java:273) ~[reactor-netty-http-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.FluxRetryWhen.subscribe(FluxRetryWhen.java:77) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.MonoRetryWhen.subscribeOrReturn(MonoRetryWhen.java:46) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.InternalMonoOperator.subscribe(InternalMonoOperator.java:57) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.http.client.HttpClientConnect$MonoHttpConnect.subscribe(HttpClientConnect.java:276) ~[reactor-netty-http-1.0.30.jar:1.0.30]
        at reactor.core.publisher.InternalMonoOperator.subscribe(InternalMonoOperator.java:64) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.MonoDefer.subscribe(MonoDefer.java:52) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4490) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.block(Mono.java:1741) ~[reactor-core-3.4.28.jar:3.4.28]
        at lt.dataHandlers.SoapServiceClient.sendRequestAndGetResponse(SoapServiceClient.java:44) ~[test-classes/:?]
        at lt.dataHandlers.SoapServiceClient.sendRequestAndParseResponse(SoapServiceClient.java:20) ~[test-classes/:?]
        at lt.GetServicesLoadTest.<init>(GetServicesLoadTest.java:33) ~[test-classes/:?]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance0(Native Method) ~[?:1.8.0_382]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance(NativeConstructorAccessorImpl.java:62) ~[?:1.8.0_382]
        at sun.reflect.DelegatingConstructorAccessorImpl.newInstance(DelegatingConstructorAccessorImpl.java:45) ~[?:1.8.0_382]
        at java.lang.reflect.Constructor.newInstance(Constructor.java:423) ~[?:1.8.0_382]
        at io.gatling.app.SimulationClass$Java.params(SimulationClass.scala:35) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Runner.load(Runner.scala:72) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Runner.run(Runner.scala:57) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.start(Gatling.scala:89) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.fromArgs(Gatling.scala:51) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.main(Gatling.scala:39) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling.main(Gatling.scala) ~[gatling-app-3.9.5.jar:3.9.5]
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method) ~[?:1.8.0_382]
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62) ~[?:1.8.0_382]
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43) ~[?:1.8.0_382]
        at java.lang.reflect.Method.invoke(Method.java:498) ~[?:1.8.0_382]
        at io.gatling.plugin.util.ForkMain.runMain(ForkMain.java:67) ~[gatling-enterprise-plugin-commons-1.5.1.jar:1.5.1]
        at io.gatling.plugin.util.ForkMain.main(ForkMain.java:35) ~[gatling-enterprise-plugin-commons-1.5.1.jar:1.5.1]
 2024-03-13 13:54:59.932 WARN  [main] reactor.core.Exceptions
                        throwIfFatal detected a jvm fatal exception, which is thrown and logged below:
java.lang.UnsatisfiedLinkError: io.netty.channel.unix.LimitsStaticallyReferencedJniMethods.iovMax()I
        at io.netty.channel.unix.LimitsStaticallyReferencedJniMethods.iovMax(Native Method) ~[netty-transport-native-unix-common-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.unix.Limits.<clinit>(Limits.java:24) ~[netty-transport-native-unix-common-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollChannelConfig.<init>(EpollChannelConfig.java:36) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollSocketChannelConfig.<init>(EpollSocketChannelConfig.java:48) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollSocketChannel.<init>(EpollSocketChannel.java:51) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at reactor.netty.resources.DefaultLoopEpoll.getChannel(DefaultLoopEpoll.java:51) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.LoopResources.onChannel(LoopResources.java:243) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.tcp.TcpResources.onChannel(TcpResources.java:251) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConfig.lambda$connectionFactory$1(TransportConfig.java:266) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.doInitAndRegister(TransportConnector.java:282) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.connect(TransportConnector.java:164) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.connect(TransportConnector.java:123) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.DefaultPooledConnectionProvider$PooledConnectionAllocator.lambda$connectChannel$0(DefaultPooledConnectionProvider.java:519) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4490) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribeWith(Mono.java:4605) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4457) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4393) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.drainLoop(SimpleDequePool.java:437) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.pendingOffer(SimpleDequePool.java:600) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.doAcquire(SimpleDequePool.java:296) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.AbstractPool$Borrower.request(AbstractPool.java:430) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.DefaultPooledConnectionProvider$DisposableAcquire.onSubscribe(DefaultPooledConnectionProvider.java:204) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool$QueueBorrowerMono.subscribe(SimpleDequePool.java:720) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.PooledConnectionProvider.lambda$acquire$2(PooledConnectionProvider.java:170) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.http.client.HttpClientConnect$MonoHttpConnect.lambda$subscribe$0(HttpClientConnect.java:273) ~[reactor-netty-http-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.FluxRetryWhen.subscribe(FluxRetryWhen.java:77) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.MonoRetryWhen.subscribeOrReturn(MonoRetryWhen.java:46) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.InternalMonoOperator.subscribe(InternalMonoOperator.java:57) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.http.client.HttpClientConnect$MonoHttpConnect.subscribe(HttpClientConnect.java:276) ~[reactor-netty-http-1.0.30.jar:1.0.30]
        at reactor.core.publisher.InternalMonoOperator.subscribe(InternalMonoOperator.java:64) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.MonoDefer.subscribe(MonoDefer.java:52) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4490) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.block(Mono.java:1741) ~[reactor-core-3.4.28.jar:3.4.28]
        at lt.dataHandlers.SoapServiceClient.sendRequestAndGetResponse(SoapServiceClient.java:44) ~[test-classes/:?]
        at lt.dataHandlers.SoapServiceClient.sendRequestAndParseResponse(SoapServiceClient.java:20) ~[test-classes/:?]
        at lt.GetServicesLoadTest.<init>(GetServicesLoadTest.java:33) ~[test-classes/:?]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance0(Native Method) ~[?:1.8.0_382]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance(NativeConstructorAccessorImpl.java:62) ~[?:1.8.0_382]
        at sun.reflect.DelegatingConstructorAccessorImpl.newInstance(DelegatingConstructorAccessorImpl.java:45) ~[?:1.8.0_382]
        at java.lang.reflect.Constructor.newInstance(Constructor.java:423) ~[?:1.8.0_382]
        at io.gatling.app.SimulationClass$Java.params(SimulationClass.scala:35) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Runner.load(Runner.scala:72) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Runner.run(Runner.scala:57) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.start(Gatling.scala:89) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.fromArgs(Gatling.scala:51) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.main(Gatling.scala:39) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling.main(Gatling.scala) ~[gatling-app-3.9.5.jar:3.9.5]
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method) ~[?:1.8.0_382]
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62) ~[?:1.8.0_382]
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43) ~[?:1.8.0_382]
        at java.lang.reflect.Method.invoke(Method.java:498) ~[?:1.8.0_382]
        at io.gatling.plugin.util.ForkMain.runMain(ForkMain.java:67) ~[gatling-enterprise-plugin-commons-1.5.1.jar:1.5.1]
        at io.gatling.plugin.util.ForkMain.main(ForkMain.java:35) ~[gatling-enterprise-plugin-commons-1.5.1.jar:1.5.1]
 2024-03-13 13:54:59.932 WARN  [main] reactor.core.Exceptions
                        throwIfFatal detected a jvm fatal exception, which is thrown and logged below:
java.lang.UnsatisfiedLinkError: io.netty.channel.unix.LimitsStaticallyReferencedJniMethods.iovMax()I
        at io.netty.channel.unix.LimitsStaticallyReferencedJniMethods.iovMax(Native Method) ~[netty-transport-native-unix-common-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.unix.Limits.<clinit>(Limits.java:24) ~[netty-transport-native-unix-common-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollChannelConfig.<init>(EpollChannelConfig.java:36) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollSocketChannelConfig.<init>(EpollSocketChannelConfig.java:48) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollSocketChannel.<init>(EpollSocketChannel.java:51) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at reactor.netty.resources.DefaultLoopEpoll.getChannel(DefaultLoopEpoll.java:51) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.LoopResources.onChannel(LoopResources.java:243) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.tcp.TcpResources.onChannel(TcpResources.java:251) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConfig.lambda$connectionFactory$1(TransportConfig.java:266) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.doInitAndRegister(TransportConnector.java:282) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.connect(TransportConnector.java:164) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.connect(TransportConnector.java:123) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.DefaultPooledConnectionProvider$PooledConnectionAllocator.lambda$connectChannel$0(DefaultPooledConnectionProvider.java:519) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4490) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribeWith(Mono.java:4605) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4457) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4393) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.drainLoop(SimpleDequePool.java:437) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.pendingOffer(SimpleDequePool.java:600) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.doAcquire(SimpleDequePool.java:296) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.AbstractPool$Borrower.request(AbstractPool.java:430) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.DefaultPooledConnectionProvider$DisposableAcquire.onSubscribe(DefaultPooledConnectionProvider.java:204) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool$QueueBorrowerMono.subscribe(SimpleDequePool.java:720) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.PooledConnectionProvider.lambda$acquire$2(PooledConnectionProvider.java:170) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.http.client.HttpClientConnect$MonoHttpConnect.lambda$subscribe$0(HttpClientConnect.java:273) ~[reactor-netty-http-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.FluxRetryWhen.subscribe(FluxRetryWhen.java:77) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.MonoRetryWhen.subscribeOrReturn(MonoRetryWhen.java:46) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.InternalMonoOperator.subscribe(InternalMonoOperator.java:57) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.http.client.HttpClientConnect$MonoHttpConnect.subscribe(HttpClientConnect.java:276) ~[reactor-netty-http-1.0.30.jar:1.0.30]
        at reactor.core.publisher.InternalMonoOperator.subscribe(InternalMonoOperator.java:64) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.MonoDefer.subscribe(MonoDefer.java:52) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4490) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.block(Mono.java:1741) ~[reactor-core-3.4.28.jar:3.4.28]
        at lt.dataHandlers.SoapServiceClient.sendRequestAndGetResponse(SoapServiceClient.java:44) ~[test-classes/:?]
        at lt.dataHandlers.SoapServiceClient.sendRequestAndParseResponse(SoapServiceClient.java:20) ~[test-classes/:?]
        at lt.GetServicesLoadTest.<init>(GetServicesLoadTest.java:33) ~[test-classes/:?]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance0(Native Method) ~[?:1.8.0_382]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance(NativeConstructorAccessorImpl.java:62) ~[?:1.8.0_382]
        at sun.reflect.DelegatingConstructorAccessorImpl.newInstance(DelegatingConstructorAccessorImpl.java:45) ~[?:1.8.0_382]
        at java.lang.reflect.Constructor.newInstance(Constructor.java:423) ~[?:1.8.0_382]
        at io.gatling.app.SimulationClass$Java.params(SimulationClass.scala:35) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Runner.load(Runner.scala:72) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Runner.run(Runner.scala:57) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.start(Gatling.scala:89) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.fromArgs(Gatling.scala:51) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.main(Gatling.scala:39) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling.main(Gatling.scala) ~[gatling-app-3.9.5.jar:3.9.5]
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method) ~[?:1.8.0_382]
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62) ~[?:1.8.0_382]
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43) ~[?:1.8.0_382]
        at java.lang.reflect.Method.invoke(Method.java:498) ~[?:1.8.0_382]
        at io.gatling.plugin.util.ForkMain.runMain(ForkMain.java:67) ~[gatling-enterprise-plugin-commons-1.5.1.jar:1.5.1]
        at io.gatling.plugin.util.ForkMain.main(ForkMain.java:35) ~[gatling-enterprise-plugin-commons-1.5.1.jar:1.5.1]
 2024-03-13 13:54:59.934 WARN  [main] reactor.core.Exceptions
                        throwIfFatal detected a jvm fatal exception, which is thrown and logged below:
java.lang.UnsatisfiedLinkError: io.netty.channel.unix.LimitsStaticallyReferencedJniMethods.iovMax()I
        at io.netty.channel.unix.LimitsStaticallyReferencedJniMethods.iovMax(Native Method) ~[netty-transport-native-unix-common-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.unix.Limits.<clinit>(Limits.java:24) ~[netty-transport-native-unix-common-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollChannelConfig.<init>(EpollChannelConfig.java:36) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollSocketChannelConfig.<init>(EpollSocketChannelConfig.java:48) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollSocketChannel.<init>(EpollSocketChannel.java:51) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at reactor.netty.resources.DefaultLoopEpoll.getChannel(DefaultLoopEpoll.java:51) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.LoopResources.onChannel(LoopResources.java:243) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.tcp.TcpResources.onChannel(TcpResources.java:251) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConfig.lambda$connectionFactory$1(TransportConfig.java:266) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.doInitAndRegister(TransportConnector.java:282) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.connect(TransportConnector.java:164) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.connect(TransportConnector.java:123) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.DefaultPooledConnectionProvider$PooledConnectionAllocator.lambda$connectChannel$0(DefaultPooledConnectionProvider.java:519) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4490) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribeWith(Mono.java:4605) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4457) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4393) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.drainLoop(SimpleDequePool.java:437) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.pendingOffer(SimpleDequePool.java:600) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.doAcquire(SimpleDequePool.java:296) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.AbstractPool$Borrower.request(AbstractPool.java:430) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.DefaultPooledConnectionProvider$DisposableAcquire.onSubscribe(DefaultPooledConnectionProvider.java:204) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool$QueueBorrowerMono.subscribe(SimpleDequePool.java:720) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.PooledConnectionProvider.lambda$acquire$2(PooledConnectionProvider.java:170) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.http.client.HttpClientConnect$MonoHttpConnect.lambda$subscribe$0(HttpClientConnect.java:273) ~[reactor-netty-http-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.FluxRetryWhen.subscribe(FluxRetryWhen.java:77) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.MonoRetryWhen.subscribeOrReturn(MonoRetryWhen.java:46) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.InternalMonoOperator.subscribe(InternalMonoOperator.java:57) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.http.client.HttpClientConnect$MonoHttpConnect.subscribe(HttpClientConnect.java:276) ~[reactor-netty-http-1.0.30.jar:1.0.30]
        at reactor.core.publisher.InternalMonoOperator.subscribe(InternalMonoOperator.java:64) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.MonoDefer.subscribe(MonoDefer.java:52) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4490) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.block(Mono.java:1741) ~[reactor-core-3.4.28.jar:3.4.28]
        at lt.dataHandlers.SoapServiceClient.sendRequestAndGetResponse(SoapServiceClient.java:44) ~[test-classes/:?]
        at lt.dataHandlers.SoapServiceClient.sendRequestAndParseResponse(SoapServiceClient.java:20) ~[test-classes/:?]
        at lt.GetServicesLoadTest.<init>(GetServicesLoadTest.java:33) ~[test-classes/:?]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance0(Native Method) ~[?:1.8.0_382]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance(NativeConstructorAccessorImpl.java:62) ~[?:1.8.0_382]
        at sun.reflect.DelegatingConstructorAccessorImpl.newInstance(DelegatingConstructorAccessorImpl.java:45) ~[?:1.8.0_382]
        at java.lang.reflect.Constructor.newInstance(Constructor.java:423) ~[?:1.8.0_382]
        at io.gatling.app.SimulationClass$Java.params(SimulationClass.scala:35) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Runner.load(Runner.scala:72) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Runner.run(Runner.scala:57) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.start(Gatling.scala:89) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.fromArgs(Gatling.scala:51) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.main(Gatling.scala:39) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling.main(Gatling.scala) ~[gatling-app-3.9.5.jar:3.9.5]
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method) ~[?:1.8.0_382]
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62) ~[?:1.8.0_382]
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43) ~[?:1.8.0_382]
        at java.lang.reflect.Method.invoke(Method.java:498) ~[?:1.8.0_382]
        at io.gatling.plugin.util.ForkMain.runMain(ForkMain.java:67) ~[gatling-enterprise-plugin-commons-1.5.1.jar:1.5.1]
        at io.gatling.plugin.util.ForkMain.main(ForkMain.java:35) ~[gatling-enterprise-plugin-commons-1.5.1.jar:1.5.1]
 2024-03-13 13:54:59.936 WARN  [main] reactor.core.Exceptions
                        throwIfFatal detected a jvm fatal exception, which is thrown and logged below:
java.lang.UnsatisfiedLinkError: io.netty.channel.unix.LimitsStaticallyReferencedJniMethods.iovMax()I
        at io.netty.channel.unix.LimitsStaticallyReferencedJniMethods.iovMax(Native Method) ~[netty-transport-native-unix-common-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.unix.Limits.<clinit>(Limits.java:24) ~[netty-transport-native-unix-common-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollChannelConfig.<init>(EpollChannelConfig.java:36) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollSocketChannelConfig.<init>(EpollSocketChannelConfig.java:48) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollSocketChannel.<init>(EpollSocketChannel.java:51) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at reactor.netty.resources.DefaultLoopEpoll.getChannel(DefaultLoopEpoll.java:51) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.LoopResources.onChannel(LoopResources.java:243) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.tcp.TcpResources.onChannel(TcpResources.java:251) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConfig.lambda$connectionFactory$1(TransportConfig.java:266) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.doInitAndRegister(TransportConnector.java:282) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.connect(TransportConnector.java:164) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.connect(TransportConnector.java:123) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.DefaultPooledConnectionProvider$PooledConnectionAllocator.lambda$connectChannel$0(DefaultPooledConnectionProvider.java:519) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4490) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribeWith(Mono.java:4605) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4457) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4393) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.drainLoop(SimpleDequePool.java:437) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.pendingOffer(SimpleDequePool.java:600) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.doAcquire(SimpleDequePool.java:296) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.AbstractPool$Borrower.request(AbstractPool.java:430) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.DefaultPooledConnectionProvider$DisposableAcquire.onSubscribe(DefaultPooledConnectionProvider.java:204) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool$QueueBorrowerMono.subscribe(SimpleDequePool.java:720) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.PooledConnectionProvider.lambda$acquire$2(PooledConnectionProvider.java:170) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.http.client.HttpClientConnect$MonoHttpConnect.lambda$subscribe$0(HttpClientConnect.java:273) ~[reactor-netty-http-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.FluxRetryWhen.subscribe(FluxRetryWhen.java:77) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.MonoRetryWhen.subscribeOrReturn(MonoRetryWhen.java:46) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.InternalMonoOperator.subscribe(InternalMonoOperator.java:57) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.http.client.HttpClientConnect$MonoHttpConnect.subscribe(HttpClientConnect.java:276) ~[reactor-netty-http-1.0.30.jar:1.0.30]
        at reactor.core.publisher.InternalMonoOperator.subscribe(InternalMonoOperator.java:64) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.MonoDefer.subscribe(MonoDefer.java:52) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4490) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.block(Mono.java:1741) ~[reactor-core-3.4.28.jar:3.4.28]
        at lt.dataHandlers.SoapServiceClient.sendRequestAndGetResponse(SoapServiceClient.java:44) ~[test-classes/:?]
        at lt.dataHandlers.SoapServiceClient.sendRequestAndParseResponse(SoapServiceClient.java:20) ~[test-classes/:?]
        at lt.GetServicesLoadTest.<init>(GetServicesLoadTest.java:33) ~[test-classes/:?]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance0(Native Method) ~[?:1.8.0_382]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance(NativeConstructorAccessorImpl.java:62) ~[?:1.8.0_382]
        at sun.reflect.DelegatingConstructorAccessorImpl.newInstance(DelegatingConstructorAccessorImpl.java:45) ~[?:1.8.0_382]
        at java.lang.reflect.Constructor.newInstance(Constructor.java:423) ~[?:1.8.0_382]
        at io.gatling.app.SimulationClass$Java.params(SimulationClass.scala:35) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Runner.load(Runner.scala:72) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Runner.run(Runner.scala:57) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.start(Gatling.scala:89) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.fromArgs(Gatling.scala:51) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.main(Gatling.scala:39) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling.main(Gatling.scala) ~[gatling-app-3.9.5.jar:3.9.5]
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method) ~[?:1.8.0_382]
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62) ~[?:1.8.0_382]
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43) ~[?:1.8.0_382]
        at java.lang.reflect.Method.invoke(Method.java:498) ~[?:1.8.0_382]
        at io.gatling.plugin.util.ForkMain.runMain(ForkMain.java:67) ~[gatling-enterprise-plugin-commons-1.5.1.jar:1.5.1]
        at io.gatling.plugin.util.ForkMain.main(ForkMain.java:35) ~[gatling-enterprise-plugin-commons-1.5.1.jar:1.5.1]
 2024-03-13 13:54:59.939 WARN  [main] reactor.core.Exceptions
                        throwIfFatal detected a jvm fatal exception, which is thrown and logged below:
java.lang.UnsatisfiedLinkError: io.netty.channel.unix.LimitsStaticallyReferencedJniMethods.iovMax()I
        at io.netty.channel.unix.LimitsStaticallyReferencedJniMethods.iovMax(Native Method) ~[netty-transport-native-unix-common-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.unix.Limits.<clinit>(Limits.java:24) ~[netty-transport-native-unix-common-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollChannelConfig.<init>(EpollChannelConfig.java:36) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollSocketChannelConfig.<init>(EpollSocketChannelConfig.java:48) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollSocketChannel.<init>(EpollSocketChannel.java:51) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at reactor.netty.resources.DefaultLoopEpoll.getChannel(DefaultLoopEpoll.java:51) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.LoopResources.onChannel(LoopResources.java:243) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.tcp.TcpResources.onChannel(TcpResources.java:251) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConfig.lambda$connectionFactory$1(TransportConfig.java:266) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.doInitAndRegister(TransportConnector.java:282) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.connect(TransportConnector.java:164) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.connect(TransportConnector.java:123) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.DefaultPooledConnectionProvider$PooledConnectionAllocator.lambda$connectChannel$0(DefaultPooledConnectionProvider.java:519) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4490) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribeWith(Mono.java:4605) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4457) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4393) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.drainLoop(SimpleDequePool.java:437) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.pendingOffer(SimpleDequePool.java:600) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.doAcquire(SimpleDequePool.java:296) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.AbstractPool$Borrower.request(AbstractPool.java:430) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.DefaultPooledConnectionProvider$DisposableAcquire.onSubscribe(DefaultPooledConnectionProvider.java:204) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool$QueueBorrowerMono.subscribe(SimpleDequePool.java:720) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.PooledConnectionProvider.lambda$acquire$2(PooledConnectionProvider.java:170) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.http.client.HttpClientConnect$MonoHttpConnect.lambda$subscribe$0(HttpClientConnect.java:273) ~[reactor-netty-http-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.FluxRetryWhen.subscribe(FluxRetryWhen.java:77) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.MonoRetryWhen.subscribeOrReturn(MonoRetryWhen.java:46) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.InternalMonoOperator.subscribe(InternalMonoOperator.java:57) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.http.client.HttpClientConnect$MonoHttpConnect.subscribe(HttpClientConnect.java:276) ~[reactor-netty-http-1.0.30.jar:1.0.30]
        at reactor.core.publisher.InternalMonoOperator.subscribe(InternalMonoOperator.java:64) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.MonoDefer.subscribe(MonoDefer.java:52) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4490) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.block(Mono.java:1741) ~[reactor-core-3.4.28.jar:3.4.28]
        at lt.dataHandlers.SoapServiceClient.sendRequestAndGetResponse(SoapServiceClient.java:44) ~[test-classes/:?]
        at lt.dataHandlers.SoapServiceClient.sendRequestAndParseResponse(SoapServiceClient.java:20) ~[test-classes/:?]
        at lt.GetServicesLoadTest.<init>(GetServicesLoadTest.java:33) ~[test-classes/:?]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance0(Native Method) ~[?:1.8.0_382]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance(NativeConstructorAccessorImpl.java:62) ~[?:1.8.0_382]
        at sun.reflect.DelegatingConstructorAccessorImpl.newInstance(DelegatingConstructorAccessorImpl.java:45) ~[?:1.8.0_382]
        at java.lang.reflect.Constructor.newInstance(Constructor.java:423) ~[?:1.8.0_382]
        at io.gatling.app.SimulationClass$Java.params(SimulationClass.scala:35) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Runner.load(Runner.scala:72) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Runner.run(Runner.scala:57) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.start(Gatling.scala:89) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.fromArgs(Gatling.scala:51) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.main(Gatling.scala:39) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling.main(Gatling.scala) ~[gatling-app-3.9.5.jar:3.9.5]
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method) ~[?:1.8.0_382]
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62) ~[?:1.8.0_382]
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43) ~[?:1.8.0_382]
        at java.lang.reflect.Method.invoke(Method.java:498) ~[?:1.8.0_382]
        at io.gatling.plugin.util.ForkMain.runMain(ForkMain.java:67) ~[gatling-enterprise-plugin-commons-1.5.1.jar:1.5.1]
        at io.gatling.plugin.util.ForkMain.main(ForkMain.java:35) ~[gatling-enterprise-plugin-commons-1.5.1.jar:1.5.1]
 2024-03-13 13:54:59.940 WARN  [main] reactor.core.Exceptions
                        throwIfFatal detected a jvm fatal exception, which is thrown and logged below:
java.lang.UnsatisfiedLinkError: io.netty.channel.unix.LimitsStaticallyReferencedJniMethods.iovMax()I
        at io.netty.channel.unix.LimitsStaticallyReferencedJniMethods.iovMax(Native Method) ~[netty-transport-native-unix-common-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.unix.Limits.<clinit>(Limits.java:24) ~[netty-transport-native-unix-common-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollChannelConfig.<init>(EpollChannelConfig.java:36) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollSocketChannelConfig.<init>(EpollSocketChannelConfig.java:48) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollSocketChannel.<init>(EpollSocketChannel.java:51) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at reactor.netty.resources.DefaultLoopEpoll.getChannel(DefaultLoopEpoll.java:51) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.LoopResources.onChannel(LoopResources.java:243) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.tcp.TcpResources.onChannel(TcpResources.java:251) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConfig.lambda$connectionFactory$1(TransportConfig.java:266) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.doInitAndRegister(TransportConnector.java:282) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.connect(TransportConnector.java:164) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.connect(TransportConnector.java:123) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.DefaultPooledConnectionProvider$PooledConnectionAllocator.lambda$connectChannel$0(DefaultPooledConnectionProvider.java:519) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4490) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribeWith(Mono.java:4605) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4457) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4393) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.drainLoop(SimpleDequePool.java:437) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.pendingOffer(SimpleDequePool.java:600) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.doAcquire(SimpleDequePool.java:296) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.AbstractPool$Borrower.request(AbstractPool.java:430) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.DefaultPooledConnectionProvider$DisposableAcquire.onSubscribe(DefaultPooledConnectionProvider.java:204) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool$QueueBorrowerMono.subscribe(SimpleDequePool.java:720) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.PooledConnectionProvider.lambda$acquire$2(PooledConnectionProvider.java:170) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.http.client.HttpClientConnect$MonoHttpConnect.lambda$subscribe$0(HttpClientConnect.java:273) ~[reactor-netty-http-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.FluxRetryWhen.subscribe(FluxRetryWhen.java:77) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.MonoRetryWhen.subscribeOrReturn(MonoRetryWhen.java:46) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.InternalMonoOperator.subscribe(InternalMonoOperator.java:57) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.http.client.HttpClientConnect$MonoHttpConnect.subscribe(HttpClientConnect.java:276) ~[reactor-netty-http-1.0.30.jar:1.0.30]
        at reactor.core.publisher.InternalMonoOperator.subscribe(InternalMonoOperator.java:64) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.MonoDefer.subscribe(MonoDefer.java:52) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4490) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.block(Mono.java:1741) ~[reactor-core-3.4.28.jar:3.4.28]
        at lt.dataHandlers.SoapServiceClient.sendRequestAndGetResponse(SoapServiceClient.java:44) ~[test-classes/:?]
        at lt.dataHandlers.SoapServiceClient.sendRequestAndParseResponse(SoapServiceClient.java:20) ~[test-classes/:?]
        at lt.GetServicesLoadTest.<init>(GetServicesLoadTest.java:33) ~[test-classes/:?]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance0(Native Method) ~[?:1.8.0_382]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance(NativeConstructorAccessorImpl.java:62) ~[?:1.8.0_382]
        at sun.reflect.DelegatingConstructorAccessorImpl.newInstance(DelegatingConstructorAccessorImpl.java:45) ~[?:1.8.0_382]
        at java.lang.reflect.Constructor.newInstance(Constructor.java:423) ~[?:1.8.0_382]
        at io.gatling.app.SimulationClass$Java.params(SimulationClass.scala:35) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Runner.load(Runner.scala:72) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Runner.run(Runner.scala:57) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.start(Gatling.scala:89) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.fromArgs(Gatling.scala:51) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.main(Gatling.scala:39) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling.main(Gatling.scala) ~[gatling-app-3.9.5.jar:3.9.5]
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method) ~[?:1.8.0_382]
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62) ~[?:1.8.0_382]
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43) ~[?:1.8.0_382]
        at java.lang.reflect.Method.invoke(Method.java:498) ~[?:1.8.0_382]
        at io.gatling.plugin.util.ForkMain.runMain(ForkMain.java:67) ~[gatling-enterprise-plugin-commons-1.5.1.jar:1.5.1]
        at io.gatling.plugin.util.ForkMain.main(ForkMain.java:35) ~[gatling-enterprise-plugin-commons-1.5.1.jar:1.5.1]
 2024-03-13 13:54:59.941 WARN  [main] reactor.core.Exceptions
                        throwIfFatal detected a jvm fatal exception, which is thrown and logged below:
java.lang.UnsatisfiedLinkError: io.netty.channel.unix.LimitsStaticallyReferencedJniMethods.iovMax()I
        at io.netty.channel.unix.LimitsStaticallyReferencedJniMethods.iovMax(Native Method) ~[netty-transport-native-unix-common-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.unix.Limits.<clinit>(Limits.java:24) ~[netty-transport-native-unix-common-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollChannelConfig.<init>(EpollChannelConfig.java:36) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollSocketChannelConfig.<init>(EpollSocketChannelConfig.java:48) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollSocketChannel.<init>(EpollSocketChannel.java:51) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at reactor.netty.resources.DefaultLoopEpoll.getChannel(DefaultLoopEpoll.java:51) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.LoopResources.onChannel(LoopResources.java:243) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.tcp.TcpResources.onChannel(TcpResources.java:251) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConfig.lambda$connectionFactory$1(TransportConfig.java:266) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.doInitAndRegister(TransportConnector.java:282) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.connect(TransportConnector.java:164) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.connect(TransportConnector.java:123) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.DefaultPooledConnectionProvider$PooledConnectionAllocator.lambda$connectChannel$0(DefaultPooledConnectionProvider.java:519) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4490) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribeWith(Mono.java:4605) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4457) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4393) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.drainLoop(SimpleDequePool.java:437) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.pendingOffer(SimpleDequePool.java:600) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.doAcquire(SimpleDequePool.java:296) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.AbstractPool$Borrower.request(AbstractPool.java:430) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.DefaultPooledConnectionProvider$DisposableAcquire.onSubscribe(DefaultPooledConnectionProvider.java:204) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool$QueueBorrowerMono.subscribe(SimpleDequePool.java:720) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.PooledConnectionProvider.lambda$acquire$2(PooledConnectionProvider.java:170) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.http.client.HttpClientConnect$MonoHttpConnect.lambda$subscribe$0(HttpClientConnect.java:273) ~[reactor-netty-http-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.FluxRetryWhen.subscribe(FluxRetryWhen.java:77) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.MonoRetryWhen.subscribeOrReturn(MonoRetryWhen.java:46) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.InternalMonoOperator.subscribe(InternalMonoOperator.java:57) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.http.client.HttpClientConnect$MonoHttpConnect.subscribe(HttpClientConnect.java:276) ~[reactor-netty-http-1.0.30.jar:1.0.30]
        at reactor.core.publisher.InternalMonoOperator.subscribe(InternalMonoOperator.java:64) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.MonoDefer.subscribe(MonoDefer.java:52) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4490) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.block(Mono.java:1741) ~[reactor-core-3.4.28.jar:3.4.28]
        at lt.dataHandlers.SoapServiceClient.sendRequestAndGetResponse(SoapServiceClient.java:44) ~[test-classes/:?]
        at lt.dataHandlers.SoapServiceClient.sendRequestAndParseResponse(SoapServiceClient.java:20) ~[test-classes/:?]
        at lt.GetServicesLoadTest.<init>(GetServicesLoadTest.java:33) ~[test-classes/:?]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance0(Native Method) ~[?:1.8.0_382]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance(NativeConstructorAccessorImpl.java:62) ~[?:1.8.0_382]
        at sun.reflect.DelegatingConstructorAccessorImpl.newInstance(DelegatingConstructorAccessorImpl.java:45) ~[?:1.8.0_382]
        at java.lang.reflect.Constructor.newInstance(Constructor.java:423) ~[?:1.8.0_382]
        at io.gatling.app.SimulationClass$Java.params(SimulationClass.scala:35) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Runner.load(Runner.scala:72) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Runner.run(Runner.scala:57) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.start(Gatling.scala:89) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.fromArgs(Gatling.scala:51) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.main(Gatling.scala:39) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling.main(Gatling.scala) ~[gatling-app-3.9.5.jar:3.9.5]
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method) ~[?:1.8.0_382]
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62) ~[?:1.8.0_382]
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43) ~[?:1.8.0_382]
        at java.lang.reflect.Method.invoke(Method.java:498) ~[?:1.8.0_382]
        at io.gatling.plugin.util.ForkMain.runMain(ForkMain.java:67) ~[gatling-enterprise-plugin-commons-1.5.1.jar:1.5.1]
        at io.gatling.plugin.util.ForkMain.main(ForkMain.java:35) ~[gatling-enterprise-plugin-commons-1.5.1.jar:1.5.1]
 2024-03-13 13:54:59.942 DEBUG [main] reactor.core.publisher.Operators
                        Duplicate Subscription has been detected
java.lang.IllegalStateException: Spec. Rule 2.12 - Subscriber.onSubscribe MUST NOT be called more than once (based on object equality)
        at reactor.core.Exceptions.duplicateOnSubscribeException(Exceptions.java:184) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Operators.reportSubscriptionSet(Operators.java:1121) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Operators.setOnce(Operators.java:1226) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.MonoFlatMap$FlatMapMain.onSubscribe(MonoFlatMap.java:109) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Operators.reportThrowInSubscribe(Operators.java:226) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4493) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.block(Mono.java:1741) ~[reactor-core-3.4.28.jar:3.4.28]
        at lt.dataHandlers.SoapServiceClient.sendRequestAndGetResponse(SoapServiceClient.java:44) ~[test-classes/:?]
        at lt.dataHandlers.SoapServiceClient.sendRequestAndParseResponse(SoapServiceClient.java:20) ~[test-classes/:?]
        at lt.GetServicesLoadTest.<init>(GetServicesLoadTest.java:33) ~[test-classes/:?]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance0(Native Method) ~[?:1.8.0_382]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance(NativeConstructorAccessorImpl.java:62) ~[?:1.8.0_382]
        at sun.reflect.DelegatingConstructorAccessorImpl.newInstance(DelegatingConstructorAccessorImpl.java:45) ~[?:1.8.0_382]
        at java.lang.reflect.Constructor.newInstance(Constructor.java:423) ~[?:1.8.0_382]
        at io.gatling.app.SimulationClass$Java.params(SimulationClass.scala:35) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Runner.load(Runner.scala:72) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Runner.run(Runner.scala:57) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.start(Gatling.scala:89) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.fromArgs(Gatling.scala:51) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.main(Gatling.scala:39) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling.main(Gatling.scala) ~[gatling-app-3.9.5.jar:3.9.5]
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method) ~[?:1.8.0_382]
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62) ~[?:1.8.0_382]
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43) ~[?:1.8.0_382]
        at java.lang.reflect.Method.invoke(Method.java:498) ~[?:1.8.0_382]
        at io.gatling.plugin.util.ForkMain.runMain(ForkMain.java:67) ~[gatling-enterprise-plugin-commons-1.5.1.jar:1.5.1]
        at io.gatling.plugin.util.ForkMain.main(ForkMain.java:35) ~[gatling-enterprise-plugin-commons-1.5.1.jar:1.5.1]
 2024-03-13 13:54:59.942 WARN  [main] reactor.core.Exceptions
                        throwIfFatal detected a jvm fatal exception, which is thrown and logged below:
java.lang.UnsatisfiedLinkError: io.netty.channel.unix.LimitsStaticallyReferencedJniMethods.iovMax()I
        at io.netty.channel.unix.LimitsStaticallyReferencedJniMethods.iovMax(Native Method) ~[netty-transport-native-unix-common-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.unix.Limits.<clinit>(Limits.java:24) ~[netty-transport-native-unix-common-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollChannelConfig.<init>(EpollChannelConfig.java:36) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollSocketChannelConfig.<init>(EpollSocketChannelConfig.java:48) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollSocketChannel.<init>(EpollSocketChannel.java:51) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at reactor.netty.resources.DefaultLoopEpoll.getChannel(DefaultLoopEpoll.java:51) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.LoopResources.onChannel(LoopResources.java:243) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.tcp.TcpResources.onChannel(TcpResources.java:251) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConfig.lambda$connectionFactory$1(TransportConfig.java:266) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.doInitAndRegister(TransportConnector.java:282) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.connect(TransportConnector.java:164) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.connect(TransportConnector.java:123) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.DefaultPooledConnectionProvider$PooledConnectionAllocator.lambda$connectChannel$0(DefaultPooledConnectionProvider.java:519) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4490) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribeWith(Mono.java:4605) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4457) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4393) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.drainLoop(SimpleDequePool.java:437) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.pendingOffer(SimpleDequePool.java:600) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.doAcquire(SimpleDequePool.java:296) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.AbstractPool$Borrower.request(AbstractPool.java:430) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.DefaultPooledConnectionProvider$DisposableAcquire.onSubscribe(DefaultPooledConnectionProvider.java:204) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool$QueueBorrowerMono.subscribe(SimpleDequePool.java:720) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.PooledConnectionProvider.lambda$acquire$2(PooledConnectionProvider.java:170) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.http.client.HttpClientConnect$MonoHttpConnect.lambda$subscribe$0(HttpClientConnect.java:273) ~[reactor-netty-http-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.FluxRetryWhen.subscribe(FluxRetryWhen.java:77) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.MonoRetryWhen.subscribeOrReturn(MonoRetryWhen.java:46) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.InternalMonoOperator.subscribe(InternalMonoOperator.java:57) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.http.client.HttpClientConnect$MonoHttpConnect.subscribe(HttpClientConnect.java:276) ~[reactor-netty-http-1.0.30.jar:1.0.30]
        at reactor.core.publisher.InternalMonoOperator.subscribe(InternalMonoOperator.java:64) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.MonoDefer.subscribe(MonoDefer.java:52) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4490) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.block(Mono.java:1741) ~[reactor-core-3.4.28.jar:3.4.28]
        at lt.dataHandlers.SoapServiceClient.sendRequestAndGetResponse(SoapServiceClient.java:44) ~[test-classes/:?]
        at lt.dataHandlers.SoapServiceClient.sendRequestAndParseResponse(SoapServiceClient.java:20) ~[test-classes/:?]
        at lt.GetServicesLoadTest.<init>(GetServicesLoadTest.java:33) ~[test-classes/:?]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance0(Native Method) ~[?:1.8.0_382]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance(NativeConstructorAccessorImpl.java:62) ~[?:1.8.0_382]
        at sun.reflect.DelegatingConstructorAccessorImpl.newInstance(DelegatingConstructorAccessorImpl.java:45) ~[?:1.8.0_382]
        at java.lang.reflect.Constructor.newInstance(Constructor.java:423) ~[?:1.8.0_382]
        at io.gatling.app.SimulationClass$Java.params(SimulationClass.scala:35) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Runner.load(Runner.scala:72) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Runner.run(Runner.scala:57) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.start(Gatling.scala:89) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.fromArgs(Gatling.scala:51) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.main(Gatling.scala:39) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling.main(Gatling.scala) ~[gatling-app-3.9.5.jar:3.9.5]
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method) ~[?:1.8.0_382]
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62) ~[?:1.8.0_382]
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43) ~[?:1.8.0_382]
        at java.lang.reflect.Method.invoke(Method.java:498) ~[?:1.8.0_382]
        at io.gatling.plugin.util.ForkMain.runMain(ForkMain.java:67) ~[gatling-enterprise-plugin-commons-1.5.1.jar:1.5.1]
        at io.gatling.plugin.util.ForkMain.main(ForkMain.java:35) ~[gatling-enterprise-plugin-commons-1.5.1.jar:1.5.1]
 2024-03-13 13:54:59.943 ERROR [main] io.gatling.app.Gatling$
                        Run crashed
java.lang.reflect.InvocationTargetException: null
        at sun.reflect.NativeConstructorAccessorImpl.newInstance0(Native Method) ~[?:1.8.0_382]
        at sun.reflect.NativeConstructorAccessorImpl.newInstance(NativeConstructorAccessorImpl.java:62) ~[?:1.8.0_382]
        at sun.reflect.DelegatingConstructorAccessorImpl.newInstance(DelegatingConstructorAccessorImpl.java:45) ~[?:1.8.0_382]
        at java.lang.reflect.Constructor.newInstance(Constructor.java:423) ~[?:1.8.0_382]
        at io.gatling.app.SimulationClass$Java.params(SimulationClass.scala:35) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Runner.load(Runner.scala:72) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Runner.run(Runner.scala:57) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.start(Gatling.scala:89) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.fromArgs(Gatling.scala:51) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling$.main(Gatling.scala:39) ~[gatling-app-3.9.5.jar:3.9.5]
        at io.gatling.app.Gatling.main(Gatling.scala) ~[gatling-app-3.9.5.jar:3.9.5]
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method) ~[?:1.8.0_382]
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62) ~[?:1.8.0_382]
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43) ~[?:1.8.0_382]
        at java.lang.reflect.Method.invoke(Method.java:498) ~[?:1.8.0_382]
        at io.gatling.plugin.util.ForkMain.runMain(ForkMain.java:67) ~[gatling-enterprise-plugin-commons-1.5.1.jar:1.5.1]
        at io.gatling.plugin.util.ForkMain.main(ForkMain.java:35) ~[gatling-enterprise-plugin-commons-1.5.1.jar:1.5.1]
Caused by: java.lang.UnsatisfiedLinkError: io.netty.channel.unix.LimitsStaticallyReferencedJniMethods.iovMax()I
        at io.netty.channel.unix.LimitsStaticallyReferencedJniMethods.iovMax(Native Method) ~[netty-transport-native-unix-common-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.unix.Limits.<clinit>(Limits.java:24) ~[netty-transport-native-unix-common-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollChannelConfig.<init>(EpollChannelConfig.java:36) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollSocketChannelConfig.<init>(EpollSocketChannelConfig.java:48) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at io.netty.channel.epoll.EpollSocketChannel.<init>(EpollSocketChannel.java:51) ~[netty-transport-classes-epoll-4.1.90.Final.jar:4.1.90.Final]
        at reactor.netty.resources.DefaultLoopEpoll.getChannel(DefaultLoopEpoll.java:51) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.LoopResources.onChannel(LoopResources.java:243) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.tcp.TcpResources.onChannel(TcpResources.java:251) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConfig.lambda$connectionFactory$1(TransportConfig.java:266) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.doInitAndRegister(TransportConnector.java:282) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.connect(TransportConnector.java:164) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.transport.TransportConnector.connect(TransportConnector.java:123) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.DefaultPooledConnectionProvider$PooledConnectionAllocator.lambda$connectChannel$0(DefaultPooledConnectionProvider.java:519) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4490) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribeWith(Mono.java:4605) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4457) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4393) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.drainLoop(SimpleDequePool.java:437) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.pendingOffer(SimpleDequePool.java:600) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.doAcquire(SimpleDequePool.java:296) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.AbstractPool$Borrower.request(AbstractPool.java:430) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.DefaultPooledConnectionProvider$DisposableAcquire.onSubscribe(DefaultPooledConnectionProvider.java:204) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool$QueueBorrowerMono.subscribe(SimpleDequePool.java:720) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.netty.resources.PooledConnectionProvider.lambda$acquire$2(PooledConnectionProvider.java:170) ~[reactor-netty-core-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.http.client.HttpClientConnect$MonoHttpConnect.lambda$subscribe$0(HttpClientConnect.java:273) ~[reactor-netty-http-1.0.30.jar:1.0.30]
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.FluxRetryWhen.subscribe(FluxRetryWhen.java:77) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.MonoRetryWhen.subscribeOrReturn(MonoRetryWhen.java:46) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.InternalMonoOperator.subscribe(InternalMonoOperator.java:57) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.netty.http.client.HttpClientConnect$MonoHttpConnect.subscribe(HttpClientConnect.java:276) ~[reactor-netty-http-1.0.30.jar:1.0.30]
        at reactor.core.publisher.InternalMonoOperator.subscribe(InternalMonoOperator.java:64) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.MonoDefer.subscribe(MonoDefer.java:52) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.subscribe(Mono.java:4490) ~[reactor-core-3.4.28.jar:3.4.28]
        at reactor.core.publisher.Mono.block(Mono.java:1741) ~[reactor-core-3.4.28.jar:3.4.28]
        at lt.dataHandlers.SoapServiceClient.sendRequestAndGetResponse(SoapServiceClient.java:44) ~[test-classes/:?]
        at lt.dataHandlers.SoapServiceClient.sendRequestAndParseResponse(SoapServiceClient.java:20) ~[test-classes/:?]
        at lt.GetServicesLoadTest.<init>(GetServicesLoadTest.java:33) ~[test-classes/:?]
        ... 17 more
2024-03-13 13:55:00,155 main TRACE Log4jLoggerFactory.getContext() found anchor class akka.event.slf4j.Logger$
2024-03-13 13:55:00,190 GatlingSystem-akka.actor.default-dispatcher-6 TRACE Log4jLoggerFactory.getContext() found anchor class akka.event.slf4j.Logger$
 2024-03-13 13:55:00.194 INFO  [GatlingSystem-akka.actor.default-dispatcher-6] akka.actor.CoordinatedShutdown
                        Running CoordinatedShutdown with reason [ActorSystemTerminateReason]
java.lang.reflect.InvocationTargetException
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
        at java.lang.reflect.Method.invoke(Method.java:498)
        at io.gatling.plugin.util.ForkMain.runMain(ForkMain.java:67)
        at io.gatling.plugin.util.ForkMain.main(ForkMain.java:35)
Caused by: java.lang.reflect.InvocationTargetException
        at sun.reflect.NativeConstructorAccessorImpl.newInstance0(Native Method)
        at sun.reflect.NativeConstructorAccessorImpl.newInstance(NativeConstructorAccessorImpl.java:62)
        at sun.reflect.DelegatingConstructorAccessorImpl.newInstance(DelegatingConstructorAccessorImpl.java:45)
        at java.lang.reflect.Constructor.newInstance(Constructor.java:423)
        at io.gatling.app.SimulationClass$Java.params(SimulationClass.scala:35)
        at io.gatling.app.Runner.load(Runner.scala:72)
        at io.gatling.app.Runner.run(Runner.scala:57)
        at io.gatling.app.Gatling$.start(Gatling.scala:89)
        at io.gatling.app.Gatling$.fromArgs(Gatling.scala:51)
        at io.gatling.app.Gatling$.main(Gatling.scala:39)
        at io.gatling.app.Gatling.main(Gatling.scala)
        ... 6 more
Caused by: java.lang.UnsatisfiedLinkError: io.netty.channel.unix.LimitsStaticallyReferencedJniMethods.iovMax()I
        at io.netty.channel.unix.LimitsStaticallyReferencedJniMethods.iovMax(Native Method)
        at io.netty.channel.unix.Limits.<clinit>(Limits.java:24)
        at io.netty.channel.epoll.EpollChannelConfig.<init>(EpollChannelConfig.java:36)
        at io.netty.channel.epoll.EpollSocketChannelConfig.<init>(EpollSocketChannelConfig.java:48)
        at io.netty.channel.epoll.EpollSocketChannel.<init>(EpollSocketChannel.java:51)
        at reactor.netty.resources.DefaultLoopEpoll.getChannel(DefaultLoopEpoll.java:51)
        at reactor.netty.resources.LoopResources.onChannel(LoopResources.java:243)
        at reactor.netty.tcp.TcpResources.onChannel(TcpResources.java:251)
        at reactor.netty.transport.TransportConfig.lambda$connectionFactory$1(TransportConfig.java:266)
        at reactor.netty.transport.TransportConnector.doInitAndRegister(TransportConnector.java:282)
        at reactor.netty.transport.TransportConnector.connect(TransportConnector.java:164)
        at reactor.netty.transport.TransportConnector.connect(TransportConnector.java:123)
        at reactor.netty.resources.DefaultPooledConnectionProvider$PooledConnectionAllocator.lambda$connectChannel$0(DefaultPooledConnectionProvider.java:519)
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58)
        at reactor.core.publisher.Mono.subscribe(Mono.java:4490)
        at reactor.core.publisher.Mono.subscribeWith(Mono.java:4605)
        at reactor.core.publisher.Mono.subscribe(Mono.java:4457)
        at reactor.core.publisher.Mono.subscribe(Mono.java:4393)
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.drainLoop(SimpleDequePool.java:437)
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.pendingOffer(SimpleDequePool.java:600)
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool.doAcquire(SimpleDequePool.java:296)
        at reactor.netty.internal.shaded.reactor.pool.AbstractPool$Borrower.request(AbstractPool.java:430)
        at reactor.netty.resources.DefaultPooledConnectionProvider$DisposableAcquire.onSubscribe(DefaultPooledConnectionProvider.java:204)
        at reactor.netty.internal.shaded.reactor.pool.SimpleDequePool$QueueBorrowerMono.subscribe(SimpleDequePool.java:720)
        at reactor.netty.resources.PooledConnectionProvider.lambda$acquire$2(PooledConnectionProvider.java:170)
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58)
        at reactor.netty.http.client.HttpClientConnect$MonoHttpConnect.lambda$subscribe$0(HttpClientConnect.java:273)
        at reactor.core.publisher.MonoCreate.subscribe(MonoCreate.java:58)
        at reactor.core.publisher.FluxRetryWhen.subscribe(FluxRetryWhen.java:77)
        at reactor.core.publisher.MonoRetryWhen.subscribeOrReturn(MonoRetryWhen.java:46)
        at reactor.core.publisher.InternalMonoOperator.subscribe(InternalMonoOperator.java:57)
        at reactor.netty.http.client.HttpClientConnect$MonoHttpConnect.subscribe(HttpClientConnect.java:276)
        at reactor.core.publisher.InternalMonoOperator.subscribe(InternalMonoOperator.java:64)
        at reactor.core.publisher.MonoDefer.subscribe(MonoDefer.java:52)
        at reactor.core.publisher.Mono.subscribe(Mono.java:4490)
        at reactor.core.publisher.Mono.block(Mono.java:1741)
        at lt.dataHandlers.SoapServiceClient.sendRequestAndGetResponse(SoapServiceClient.java:44)
        at lt.dataHandlers.SoapServiceClient.sendRequestAndParseResponse(SoapServiceClient.java:20)
        at lt.GetServicesLoadTest.<init>(GetServicesLoadTest.java:33)
        ... 17 more
[INFO] ------------------------------------------------------------------------
[INFO] BUILD FAILURE
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  12:23 min
[INFO] Finished at: 2024-03-13T13:55:00+02:00
[INFO] ------------------------------------------------------------------------
[ERROR] Failed to execute goal io.gatling:gatling-maven-plugin:4.3.0:test (default-cli) on project ferrygateway: Gatling failed.: ForkException ->
 [Help 1]
org.apache.maven.lifecycle.LifecycleExecutionException: Failed to execute goal io.gatling:gatling-maven-plugin:4.3.0:test (default-cli) on project
 ferrygateway: Gatling failed.
    at org.apache.maven.lifecycle.internal.MojoExecutor.doExecute2 (MojoExecutor.java:347)
    at org.apache.maven.lifecycle.internal.MojoExecutor.doExecute (MojoExecutor.java:330)
    at org.apache.maven.lifecycle.internal.MojoExecutor.execute (MojoExecutor.java:213)
    at org.apache.maven.lifecycle.internal.MojoExecutor.execute (MojoExecutor.java:175)
    at org.apache.maven.lifecycle.internal.MojoExecutor.access$000 (MojoExecutor.java:76)
    at org.apache.maven.lifecycle.internal.MojoExecutor$1.run (MojoExecutor.java:163)
    at org.apache.maven.plugin.DefaultMojosExecutionStrategy.execute (DefaultMojosExecutionStrategy.java:39)
    at org.apache.maven.lifecycle.internal.MojoExecutor.execute (MojoExecutor.java:160)
    at org.apache.maven.lifecycle.internal.LifecycleModuleBuilder.buildProject (LifecycleModuleBuilder.java:105)
    at org.apache.maven.lifecycle.internal.LifecycleModuleBuilder.buildProject (LifecycleModuleBuilder.java:73)
    at org.apache.maven.lifecycle.internal.builder.singlethreaded.SingleThreadedBuilder.build (SingleThreadedBuilder.java:53)
    at org.apache.maven.lifecycle.internal.LifecycleStarter.execute (LifecycleStarter.java:118)
    at org.apache.maven.DefaultMaven.doExecute (DefaultMaven.java:260)
    at org.apache.maven.DefaultMaven.doExecute (DefaultMaven.java:172)
    at org.apache.maven.DefaultMaven.execute (DefaultMaven.java:100)
    at org.apache.maven.cli.MavenCli.execute (MavenCli.java:821)
    at org.apache.maven.cli.MavenCli.doMain (MavenCli.java:270)
    at org.apache.maven.cli.MavenCli.main (MavenCli.java:192)
    at sun.reflect.NativeMethodAccessorImpl.invoke0 (Native Method)
    at sun.reflect.NativeMethodAccessorImpl.invoke (NativeMethodAccessorImpl.java:62)
    at sun.reflect.DelegatingMethodAccessorImpl.invoke (DelegatingMethodAccessorImpl.java:43)
    at java.lang.reflect.Method.invoke (Method.java:498)
    at org.codehaus.plexus.classworlds.launcher.Launcher.launchEnhanced (Launcher.java:282)
    at org.codehaus.plexus.classworlds.launcher.Launcher.launch (Launcher.java:225)
    at org.codehaus.plexus.classworlds.launcher.Launcher.mainWithExitCode (Launcher.java:406)
    at org.codehaus.plexus.classworlds.launcher.Launcher.main (Launcher.java:347)
Caused by: org.apache.maven.plugin.MojoExecutionException: Gatling failed.
    at io.gatling.mojo.GatlingMojo.execute (GatlingMojo.java:181)
    at org.apache.maven.plugin.DefaultBuildPluginManager.executeMojo (DefaultBuildPluginManager.java:126)
    at org.apache.maven.lifecycle.internal.MojoExecutor.doExecute2 (MojoExecutor.java:342)
    at org.apache.maven.lifecycle.internal.MojoExecutor.doExecute (MojoExecutor.java:330)
    at org.apache.maven.lifecycle.internal.MojoExecutor.execute (MojoExecutor.java:213)
    at org.apache.maven.lifecycle.internal.MojoExecutor.execute (MojoExecutor.java:175)
    at org.apache.maven.lifecycle.internal.MojoExecutor.access$000 (MojoExecutor.java:76)
    at org.apache.maven.lifecycle.internal.MojoExecutor$1.run (MojoExecutor.java:163)
    at org.apache.maven.plugin.DefaultMojosExecutionStrategy.execute (DefaultMojosExecutionStrategy.java:39)
    at org.apache.maven.lifecycle.internal.MojoExecutor.execute (MojoExecutor.java:160)
    at org.apache.maven.lifecycle.internal.LifecycleModuleBuilder.buildProject (LifecycleModuleBuilder.java:105)
    at org.apache.maven.lifecycle.internal.LifecycleModuleBuilder.buildProject (LifecycleModuleBuilder.java:73)
    at org.apache.maven.lifecycle.internal.builder.singlethreaded.SingleThreadedBuilder.build (SingleThreadedBuilder.java:53)
    at org.apache.maven.lifecycle.internal.LifecycleStarter.execute (LifecycleStarter.java:118)
    at org.apache.maven.DefaultMaven.doExecute (DefaultMaven.java:260)
    at org.apache.maven.DefaultMaven.doExecute (DefaultMaven.java:172)
    at org.apache.maven.DefaultMaven.execute (DefaultMaven.java:100)
    at org.apache.maven.cli.MavenCli.execute (MavenCli.java:821)
    at org.apache.maven.cli.MavenCli.doMain (MavenCli.java:270)
    at org.apache.maven.cli.MavenCli.main (MavenCli.java:192)
    at sun.reflect.NativeMethodAccessorImpl.invoke0 (Native Method)
    at sun.reflect.NativeMethodAccessorImpl.invoke (NativeMethodAccessorImpl.java:62)
    at sun.reflect.DelegatingMethodAccessorImpl.invoke (DelegatingMethodAccessorImpl.java:43)
    at java.lang.reflect.Method.invoke (Method.java:498)
    at org.codehaus.plexus.classworlds.launcher.Launcher.launchEnhanced (Launcher.java:282)
    at org.codehaus.plexus.classworlds.launcher.Launcher.launch (Launcher.java:225)
    at org.codehaus.plexus.classworlds.launcher.Launcher.mainWithExitCode (Launcher.java:406)
    at org.codehaus.plexus.classworlds.launcher.Launcher.main (Launcher.java:347)
Caused by: io.gatling.plugin.util.Fork$ForkException
    at io.gatling.plugin.util.Fork.run (Fork.java:213)
    at io.gatling.mojo.GatlingMojo.executeGatling (GatlingMojo.java:252)
    at io.gatling.mojo.GatlingMojo.iterateBySimulations (GatlingMojo.java:211)
    at io.gatling.mojo.GatlingMojo.execute (GatlingMojo.java:169)
    at org.apache.maven.plugin.DefaultBuildPluginManager.executeMojo (DefaultBuildPluginManager.java:126)
    at org.apache.maven.lifecycle.internal.MojoExecutor.doExecute2 (MojoExecutor.java:342)
    at org.apache.maven.lifecycle.internal.MojoExecutor.doExecute (MojoExecutor.java:330)
    at org.apache.maven.lifecycle.internal.MojoExecutor.execute (MojoExecutor.java:213)
    at org.apache.maven.lifecycle.internal.MojoExecutor.execute (MojoExecutor.java:175)
    at org.apache.maven.lifecycle.internal.MojoExecutor.access$000 (MojoExecutor.java:76)
    at org.apache.maven.lifecycle.internal.MojoExecutor$1.run (MojoExecutor.java:163)
    at org.apache.maven.plugin.DefaultMojosExecutionStrategy.execute (DefaultMojosExecutionStrategy.java:39)
    at org.apache.maven.lifecycle.internal.MojoExecutor.execute (MojoExecutor.java:160)
    at org.apache.maven.lifecycle.internal.LifecycleModuleBuilder.buildProject (LifecycleModuleBuilder.java:105)
    at org.apache.maven.lifecycle.internal.LifecycleModuleBuilder.buildProject (LifecycleModuleBuilder.java:73)
    at org.apache.maven.lifecycle.internal.builder.singlethreaded.SingleThreadedBuilder.build (SingleThreadedBuilder.java:53)
    at org.apache.maven.lifecycle.internal.LifecycleStarter.execute (LifecycleStarter.java:118)
    at org.apache.maven.DefaultMaven.doExecute (DefaultMaven.java:260)
    at org.apache.maven.DefaultMaven.doExecute (DefaultMaven.java:172)
    at org.apache.maven.DefaultMaven.execute (DefaultMaven.java:100)
    at org.apache.maven.cli.MavenCli.execute (MavenCli.java:821)
    at org.apache.maven.cli.MavenCli.doMain (MavenCli.java:270)
    at org.apache.maven.cli.MavenCli.main (MavenCli.java:192)
    at sun.reflect.NativeMethodAccessorImpl.invoke0 (Native Method)
    at sun.reflect.NativeMethodAccessorImpl.invoke (NativeMethodAccessorImpl.java:62)
    at sun.reflect.DelegatingMethodAccessorImpl.invoke (DelegatingMethodAccessorImpl.java:43)
    at java.lang.reflect.Method.invoke (Method.java:498)
    at org.codehaus.plexus.classworlds.launcher.Launcher.launchEnhanced (Launcher.java:282)
    at org.codehaus.plexus.classworlds.launcher.Launcher.launch (Launcher.java:225)
    at org.codehaus.plexus.classworlds.launcher.Launcher.mainWithExitCode (Launcher.java:406)
    at org.codehaus.plexus.classworlds.launcher.Launcher.main (Launcher.java:347)