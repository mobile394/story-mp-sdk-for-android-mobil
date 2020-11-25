<h1 align="center">
  storyblok-mp-SDK
</h1>

<p align="center">
    ... a Storyblok Client SDK written using Kotlin Multiplatform. (Android, JVM, JS, iOS, ...)
</p>

<div align="center">
  <a href="https://github.com/mikepenz/storyblok-mp-SDK/actions">
		<img src="https://github.com/mikepenz/storyblok-mp-SDK/workflows/CI/badge.svg"/>
	</a>
</div>
<br />

-------

<p align="center">
    <a href="#whats-included-">What's included 🚀</a> &bull;
    <a href="#about-storyblok">About Storyblok</a> &bull;
    <a href="#setup">Setup 🛠️</a> &bull;
    <a href="#usage">Usage 🛠️</a> &bull;
    <a href="#license">License 📓</a>
</p>

-------

### What's included 🚀

- Super simple setup
- Cross-platform ready
- Lightweight

-------

# About Storyblok
- **WEBSITE** https://www.storyblok.com/
- **API DOC** https://www.storyblok.com/docs/api/content-delivery

-------

## Setup
### Using Gradle

<details><summary><b>JVM</b></summary>
<p>

To use the storyblok SDK on JVM, you have to include:
```kotlin
dependencies {
    implementation("com.mikepenz:storyblok-mp-sdk-jvm:${version}")
}
```

</p>
</details>

<details open><summary><b>Android</b></summary>
<p>

For Android a special dependency is provided:
```kotlin
dependencies {
    implementation("com.mikepenz:storyblok-mp-sdk-android:${version}")
}
```

</p>
</details>

<details><summary><b>iOS</b></summary>
<p>

For iOS you will have to use the Kotlin Native [support](https://github.com/JetBrains/kotlin-native) and use the following dependency:
```kotlin
dependencies {
    implementation("com.mikepenz:storyblok-mp-sdk-ios:${version}")
}
```

</p>
</details>

<details><summary><b>JS</b></summary>
<p>

For JS (node-js) applications you will have to use the Kotlin JS [support](https://kotlinlang.org/docs/tutorials/javascript/kotlin-to-javascript/kotlin-to-javascript.html) and the following dependency:

```kotlin
dependencies {
    implementation("com.mikepenz:storyblok-mp-sdk-js:${version}")
}
```

</p>
</details>


## Usage
### Init client

```kotlin
val client = Storyblok("your-storyblok-token")
```

### General

This Kotlin multi platform library uses Kotlin coroutines for the requests (similar to the ktor API).
All fetch methods are suspending functions, and need to be called respectively.

### Load a story
```kotlin
client.fetchStory("full_slug:id:uuid")
// All storyblock params are supported, see javadoc for more information
```

### Load a list of stories
```kotlin
client.fetchStories()
// All storyblock params are supported, see javadoc for more information
```

### Load current space
```kotlin
client.fetchCurrentSpace()
```

### Load a list of datasources
```kotlin
client.fetchDatasources()
// All storyblock params are supported, see javadoc for more information
```

### Load a map of datasource entries
```kotlin
client.fetchDatasourceEntries()
// All storyblock params are supported, see javadoc for more information
```

### Load a list of map of links with their uuid as key
```kotlin
client.fetchLinks()
// All storyblock params are supported, see javadoc for more information
```

### Load a list of tags
```kotlin
client.fetchTags()
// All storyblock params are supported, see javadoc for more information
```

## Libs used in android sample app:
Mike Penz:
- FastAdapter https://github.com/mikepenz/FastAdapter
- AboutLibraries https://github.com/mikepenz/AboutLibraries
- Android-Iconics https://github.com/mikepenz/Android-Iconics
- MaterialDrawer https://github.com/mikepenz/MaterialDrawer

## Developed By

* Mike Penz
 * [mikepenz.com](http://mikepenz.com) - <mikepenz@gmail.com>
 * [paypal.me/mikepenz](http://paypal.me/mikepenz)

## Contributors

This free, open source software was also made possible by a group of volunteers that put many hours of hard work into it. See the [CONTRIBUTORS.md](CONTRIBUTORS.md) file for details.

## Credits

Some parts of the Kotlin Multiplatform configurations are a result of various great resources on the internet. Including:
- https://github.com/joreilly/PeopleInSpace
- https://natanfudge.github.io/fudgedocs/publish-kotlin-mpp-lib.html
- https://github.com/Kotlin/kotlinx.serialization
- https://github.com/Kotlin/dokka
- and the official Kotlin multiplatform docs

## License

    Copyright 2020 Mike Penz

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
