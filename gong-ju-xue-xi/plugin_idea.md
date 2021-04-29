# 



## 





###  设置环境



```shell
git clone --depth 1 git://git.jetbrains.org/idea/community.git idea
```



###。

```java
Cannot create configurable

com.intellij.diagnostic.PluginException: Cannot create class org.intellij.sequencer.config.ConfigurationOptions (classloader=PluginClassLoader(plugin=PluginDescriptor(name=SequenceDiagram, id=SequenceDiagram, descriptorPath=plugin.xml, path=~/Library/Application Support/JetBrains/IntelliJIdea2021.1/plugins/SequenceDiagram, version=1.2.8, package=null), packagePrefix=null, instanceId=63, state=active))
	at com.intellij.serviceContainer.ComponentManagerImpl.instantiateClass(ComponentManagerImpl.kt:763)
	at com.intellij.serviceContainer.ComponentManagerImpl.instantiateClass(ComponentManagerImpl.kt:781)
	at com.intellij.openapi.options.ConfigurableEP$ClassProducer.createElement(ConfigurableEP.java:440)
	at com.intellij.openapi.options.ConfigurableEP.createConfigurable(ConfigurableEP.java:346)
	at com.intellij.openapi.options.ex.ConfigurableWrapper.createConfigurable(ConfigurableWrapper.java:42)
	at com.intellij.openapi.options.ex.ConfigurableWrapper.getConfigurable(ConfigurableWrapper.java:116)
	at com.intellij.openapi.options.ex.ConfigurableWrapper.cast(ConfigurableWrapper.java:91)
	at com.intellij.openapi.options.ex.ConfigurableWrapper.getDisplayName(ConfigurableWrapper.java:137)
	at com.intellij.openapi.options.newEditor.ConfigurableEditor.createDefaultContent(ConfigurableEditor.java:302)
	at com.intellij.openapi.options.newEditor.ConfigurableEditor$1.create(ConfigurableEditor.java:54)
	at com.intellij.openapi.options.newEditor.ConfigurableEditor$1.create(ConfigurableEditor.java:50)
	at com.intellij.ui.CardLayoutPanel.createValue(CardLayoutPanel.java:83)
	at com.intellij.ui.CardLayoutPanel.select(CardLayoutPanel.java:111)
	at com.intellij.ui.CardLayoutPanel.lambda$selectLater$0(CardLayoutPanel.java:127)
	at com.intellij.openapi.application.TransactionGuardImpl.runWithWritingAllowed(TransactionGuardImpl.java:218)
	at com.intellij.openapi.application.TransactionGuardImpl.access$200(TransactionGuardImpl.java:21)
	at com.intellij.openapi.application.TransactionGuardImpl$2.run(TransactionGuardImpl.java:200)
	at com.intellij.openapi.application.impl.ApplicationImpl.runIntendedWriteActionOnCurrentThread(ApplicationImpl.java:781)
	at com.intellij.openapi.application.impl.ApplicationImpl.lambda$invokeLater$4(ApplicationImpl.java:319)
	at com.intellij.openapi.application.impl.FlushQueue.doRun(FlushQueue.java:84)
	at com.intellij.openapi.application.impl.FlushQueue.runNextEvent(FlushQueue.java:133)
	at com.intellij.openapi.application.impl.FlushQueue.flushNow(FlushQueue.java:46)
	at com.intellij.openapi.application.impl.FlushQueue$FlushNow.run(FlushQueue.java:189)
	at java.desktop/java.awt.event.InvocationEvent.dispatch(InvocationEvent.java:313)
	at java.desktop/java.awt.EventQueue.dispatchEventImpl(EventQueue.java:776)
	at java.desktop/java.awt.EventQueue$4.run(EventQueue.java:727)
	at java.desktop/java.awt.EventQueue$4.run(EventQueue.java:721)
	at java.base/java.security.AccessController.doPrivileged(Native Method)
	at java.base/java.security.ProtectionDomain$JavaSecurityAccessImpl.doIntersectionPrivilege(ProtectionDomain.java:85)
	at java.desktop/java.awt.EventQueue.dispatchEvent(EventQueue.java:746)
	at com.intellij.ide.IdeEventQueue.defaultDispatchEvent(IdeEventQueue.java:969)
	at com.intellij.ide.IdeEventQueue._dispatchEvent(IdeEventQueue.java:839)
	at com.intellij.ide.IdeEventQueue.lambda$dispatchEvent$8(IdeEventQueue.java:449)
	at com.intellij.openapi.progress.impl.CoreProgressManager.computePrioritized(CoreProgressManager.java:797)
	at com.intellij.ide.IdeEventQueue.lambda$dispatchEvent$9(IdeEventQueue.java:448)
	at com.intellij.openapi.application.impl.ApplicationImpl.runIntendedWriteActionOnCurrentThread(ApplicationImpl.java:781)
	at com.intellij.ide.IdeEventQueue.dispatchEvent(IdeEventQueue.java:496)
	at java.desktop/java.awt.EventDispatchThread.pumpOneEventForFilters(EventDispatchThread.java:203)
	at java.desktop/java.awt.EventDispatchThread.pumpEventsForFilter(EventDispatchThread.java:124)
	at java.desktop/java.awt.EventDispatchThread.pumpEventsForFilter(EventDispatchThread.java:117)
	at java.desktop/java.awt.WaitDispatchSupport$2.run(WaitDispatchSupport.java:190)
	at java.desktop/java.awt.WaitDispatchSupport$4.run(WaitDispatchSupport.java:235)
	at java.desktop/java.awt.WaitDispatchSupport$4.run(WaitDispatchSupport.java:233)
	at java.base/java.security.AccessController.doPrivileged(Native Method)
	at java.desktop/java.awt.WaitDispatchSupport.enter(WaitDispatchSupport.java:233)
	at java.desktop/java.awt.Dialog.show(Dialog.java:1063)
	at com.intellij.openapi.ui.impl.DialogWrapperPeerImpl$MyDialog.show(DialogWrapperPeerImpl.java:694)
	at com.intellij.openapi.ui.impl.DialogWrapperPeerImpl.show(DialogWrapperPeerImpl.java:436)
	at com.intellij.openapi.ui.DialogWrapper.doShow(DialogWrapper.java:1702)
	at com.intellij.openapi.ui.DialogWrapper.show(DialogWrapper.java:1661)
	at com.intellij.ide.actions.ShowSettingsUtilImpl.showSettingsDialog(ShowSettingsUtilImpl.java:90)
	at com.intellij.ide.actions.ShowSettingsAction.perform(ShowSettingsAction.java:55)
	at com.intellij.ui.mac.MacOSApplicationProvider$Worker.lambda$initMacApplication$1(MacOSApplicationProvider.java:81)
	at com.intellij.ui.mac.MacOSApplicationProvider$Worker.lambda$submit$8(MacOSApplicationProvider.java:181)
	at com.intellij.openapi.application.TransactionGuardImpl.runWithWritingAllowed(TransactionGuardImpl.java:218)
	at com.intellij.openapi.application.TransactionGuardImpl.access$200(TransactionGuardImpl.java:21)
	at com.intellij.openapi.application.TransactionGuardImpl$2.run(TransactionGuardImpl.java:200)
	at com.intellij.openapi.application.impl.ApplicationImpl.runIntendedWriteActionOnCurrentThread(ApplicationImpl.java:781)
	at com.intellij.openapi.application.impl.ApplicationImpl.lambda$invokeLater$4(ApplicationImpl.java:319)
	at com.intellij.openapi.application.impl.FlushQueue.doRun(FlushQueue.java:84)
	at com.intellij.openapi.application.impl.FlushQueue.runNextEvent(FlushQueue.java:133)
	at com.intellij.openapi.application.impl.FlushQueue.flushNow(FlushQueue.java:46)
	at com.intellij.openapi.application.impl.FlushQueue$FlushNow.run(FlushQueue.java:189)
	at java.desktop/java.awt.event.InvocationEvent.dispatch(InvocationEvent.java:313)
	at java.desktop/java.awt.EventQueue.dispatchEventImpl(EventQueue.java:776)
	at java.desktop/java.awt.EventQueue$4.run(EventQueue.java:727)
	at java.desktop/java.awt.EventQueue$4.run(EventQueue.java:721)
	at java.base/java.security.AccessController.doPrivileged(Native Method)
	at java.base/java.security.ProtectionDomain$JavaSecurityAccessImpl.doIntersectionPrivilege(ProtectionDomain.java:85)
	at java.desktop/java.awt.EventQueue.dispatchEvent(EventQueue.java:746)
	at com.intellij.ide.IdeEventQueue.defaultDispatchEvent(IdeEventQueue.java:969)
	at com.intellij.ide.IdeEventQueue._dispatchEvent(IdeEventQueue.java:839)
	at com.intellij.ide.IdeEventQueue.lambda$dispatchEvent$8(IdeEventQueue.java:449)
	at com.intellij.openapi.progress.impl.CoreProgressManager.computePrioritized(CoreProgressManager.java:808)
	at com.intellij.ide.IdeEventQueue.lambda$dispatchEvent$9(IdeEventQueue.java:448)
	at com.intellij.openapi.application.impl.ApplicationImpl.runIntendedWriteActionOnCurrentThread(ApplicationImpl.java:781)
	at com.intellij.ide.IdeEventQueue.dispatchEvent(IdeEventQueue.java:496)
	at com.intellij.cloudConfig.CloudConfigManager.waitDone(CloudConfigManager.java:1856)
	at com.intellij.cloudConfig.CloudConfigManager.getRepositoryPlugin(CloudConfigManager.java:1841)
	at com.intellij.cloudConfig.CloudConfigManager.lambda$updatePlugins$45(CloudConfigManager.java:1915)
	at com.intellij.cloudConfig.CloudConfigManager.mergePlugins(CloudConfigManager.java:2082)
	at com.intellij.cloudConfig.CloudConfigManager.mergePlugins(CloudConfigManager.java:2070)
	at com.intellij.cloudConfig.CloudConfigManager.updatePlugins(CloudConfigManager.java:1917)
	at com.intellij.cloudConfig.CloudConfigManager.safeUpdatePlugins(CloudConfigManager.java:1865)
	at com.intellij.cloudConfig.CloudConfigManager.lambda$doConnection$20(CloudConfigManager.java:996)
	at com.intellij.openapi.application.TransactionGuardImpl.runWithWritingAllowed(TransactionGuardImpl.java:218)
	at com.intellij.openapi.application.TransactionGuardImpl.access$200(TransactionGuardImpl.java:21)
	at com.intellij.openapi.application.TransactionGuardImpl$2.run(TransactionGuardImpl.java:200)
	at com.intellij.openapi.application.impl.ApplicationImpl.runIntendedWriteActionOnCurrentThread(ApplicationImpl.java:781)
	at com.intellij.openapi.application.impl.ApplicationImpl.lambda$invokeLater$4(ApplicationImpl.java:319)
	at com.intellij.openapi.application.impl.FlushQueue.doRun(FlushQueue.java:84)
	at com.intellij.openapi.application.impl.FlushQueue.runNextEvent(FlushQueue.java:133)
	at com.intellij.openapi.application.impl.FlushQueue.flushNow(FlushQueue.java:46)
	at com.intellij.openapi.application.impl.FlushQueue$FlushNow.run(FlushQueue.java:189)
	at java.desktop/java.awt.event.InvocationEvent.dispatch(InvocationEvent.java:313)
	at java.desktop/java.awt.EventQueue.dispatchEventImpl(EventQueue.java:776)
	at java.desktop/java.awt.EventQueue$4.run(EventQueue.java:727)
	at java.desktop/java.awt.EventQueue$4.run(EventQueue.java:721)
	at java.base/java.security.AccessController.doPrivileged(Native Method)
	at java.base/java.security.ProtectionDomain$JavaSecurityAccessImpl.doIntersectionPrivilege(ProtectionDomain.java:85)
	at java.desktop/java.awt.EventQueue.dispatchEvent(EventQueue.java:746)
	at com.intellij.ide.IdeEventQueue.defaultDispatchEvent(IdeEventQueue.java:969)
	at com.intellij.ide.IdeEventQueue._dispatchEvent(IdeEventQueue.java:839)
	at com.intellij.ide.IdeEventQueue.lambda$dispatchEvent$8(IdeEventQueue.java:449)
	at com.intellij.openapi.progress.impl.CoreProgressManager.computePrioritized(CoreProgressManager.java:808)
	at com.intellij.ide.IdeEventQueue.lambda$dispatchEvent$9(IdeEventQueue.java:448)
	at com.intellij.openapi.application.impl.ApplicationImpl.runIntendedWriteActionOnCurrentThread(ApplicationImpl.java:781)
	at com.intellij.ide.IdeEventQueue.dispatchEvent(IdeEventQueue.java:496)
	at java.desktop/java.awt.EventDispatchThread.pumpOneEventForFilters(EventDispatchThread.java:203)
	at java.desktop/java.awt.EventDispatchThread.pumpEventsForFilter(EventDispatchThread.java:124)
	at java.desktop/java.awt.EventDispatchThread.pumpEventsForHierarchy(EventDispatchThread.java:113)
	at java.desktop/java.awt.EventDispatchThread.pumpEvents(EventDispatchThread.java:109)
	at java.desktop/java.awt.EventDispatchThread.pumpEvents(EventDispatchThread.java:101)
	at java.desktop/java.awt.EventDispatchThread.run(EventDispatchThread.java:90)
Caused by: java.lang.NoSuchMethodException: org.intellij.sequencer.config.ConfigurationOptions.<init>()
	at java.base/java.lang.Class.getConstructor0(Class.java:3349)
	at java.base/java.lang.Class.getDeclaredConstructor(Class.java:2553)
	at com.intellij.serviceContainer.ComponentManagerImpl.instantiateClass(ComponentManagerImpl.kt:720)
	... 113 more
```





### 插件配置文件说明

```xml
<projectConfigurable instance="com.yingling.extensions.component.NccDevSettingComponent"/>
```

>  FQN of implementation. See [The Configurable Interface](https://plugins.jetbrains.com/docs/intellij/settings-guide.html#the-configurable-interface) for more information.



### GRADLE中本地包引用 

```xml
dependencies {
    implementation(fileTree(mapOf("dir" to "lib", "include" to listOf("*.jar"))))
}
```

> Build.gradle.kts的 dependencies下的引用方式，直接新建lib文件夹