# Example project showcasing a bug in react-native-pdf

## Start demo project
```
npm install
// or
yarn install

react-native run-android
```

## Get react-native-pdf in a corrupted state

```
Page 1 > Page 2
```

Now pdf is loaded because of pageOffset property of viewpager.

```
> Page 2 > Page 3 > Page 2 > Page 3
```

Pdf is still loaded and can be viewed again.

```
Page 3 > Page 2 > Page 1 > Page 2 > Page 3
```

Pdf is not shown and we can't interact with pdf control.