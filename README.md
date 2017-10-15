
# react-native-image-color-picker
Image color picker: Provide image source and it will return 
- Different color palettes out of image 
- Average color palette out of image

## Getting started

Peer dependency

```sh
$ npm install react-native-fetch-blob --save
```
or

```sh
$ yarn add react-native-image-color-picker --save
```
then

```sh
$ react-native link react-native-fetch-blob
```

Package 

```sh
$ npm install react-native-image-color-picker --save
```
or

```sh
$ yarn add react-native-image-color-picker --save
```

## Usage

```jsx
import React, { Component } from 'react';
import { ImageColorPicker } from 'react-native-image-color-picker';

export default class App extends Component {

  pickerCallback = message => {
    if (message && message.nativeEvent && message.nativeEvent.data) {
      console.log(message.nativeEvent.data); // response from ImageColorPicker
    }
  };

  render() {
    return (
        ....

        <ImageColorPicker
          imageUrl="https://dummyimage.com/100x100"
          pickerCallback={this.pickerCallback}
        />

        ....
    );
  }
}
```

## Available Props/Options

- `imageUrl`: url of image 
- `pickerCallback`: callback method for ImageColorPicker Success or Failure
- (optional)`imageType`: type of image e.g. jpeg, png `Default value: jpeg`
- (optional)`paletteType`: palette type e.g `average`: for average color of image, `dominant`: dominant colors in image `Default value: dominant`
- (optional)`paletteCount`: no of color palettes need e.g. 3 dominant color palette, applicable only in case of `paletteType: 'dominant'` `Default value: 3`
- (optional)`defaultPalette`: default color palette `Default value: [0, 0, 0, 1]`
- (optional)`colorType`: color code type e.g. rgba or hex `Default value: rgba`
- (optional)`pickerStyle`: picker container styles

## TODO

- Add demo app
- Support Image picker gallery

## Contributing

Interested in contributing to this repository? PR are most welcome!
