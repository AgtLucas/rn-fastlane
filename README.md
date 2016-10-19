# rn-fastlane

Setting up Fastlane

Install fastlane:

```sh
$ gem install fastlane --verbose
```

## Step 1

* Create a private repo to store all the certs/profiles

Init match and point your private repo url
```sh
$ match init
```

* Create your app id

```sh
$ produce -u <your user email> -a <your bundle id>
```

* Generate all the certs/profiles

*This is the command you would run on a new computer or new developer’s computer*

```sh
$ match appstore
```

## Step 2

* Create our Fastfile

```sh
$ fastlane init
```

## Step 3

* Configure Xcode to auto-increment build version (see step 1 and 2)

[https://developer.apple.com/library/content/qa/qa1827/_index.html](https://developer.apple.com/library/content/qa/qa1827/_index.html)

* Code signing

Use Automatic on `Provisioning Profile`
```
$(sigh_’ + bundle_id + ‘_appstore’)
```

## Step 4

Done!

```sh
$ fastlane beta
```

---

## References

* [Fastlane](https://fastlane.tools/)
* [Infinite Red - Simple React Native iOS Releases](https://shift.infinite.red/simple-react-native-ios-releases-4c28bb53a97b#.ar38yyso7)
* [Deploying a React Native App with Fastlane - Part 1](https://dbanck.svbtle.com/deploying-a-react-native-app-with-fastlane)
* [Deploying a React Native App with Fastlane - Part 2](https://dbanck.svbtle.com/part-2-android-with-fastlane-supply)
