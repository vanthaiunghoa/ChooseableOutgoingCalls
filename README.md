This is an [Xposed module](http://repo.xposed.info/) with a workaround for [Android Bug #58097](https://code.google.com/p/android/issues/detail?id=58097). It replaces the [getCallIntent() method of com.android.contacts.common.CallUtil](https://android.googlesource.com/platform/packages/apps/ContactsCommon/+/master/src/com/android/contacts/common/CallUtil.java) with a version that creates a `android.intent.action.VIEW` intent without a specific component set instead. This is not exactly what earlier Android versions used to do, but `ACTION_CALL_PRIVILEGED` is [for some privileged apps only](http://stackoverflow.com/a/8567388/1881610) now, so we can't use that anymore.

The binary version is available [on the releases page](https://github.com/phillipberndt/ChooseableOutgoingCalls/releases), [here](https://github.com/phillipberndt/ChooseableOutgoingCalls/releases/download/v1.0/ChooseableOutgoingCalls.apk).