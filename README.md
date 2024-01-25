# React Native Barcode Creator Fixed

**Note:** This repository is a fork of the [react-native-barcode-creator](https://github.com/VittoriDavide/react-native-barcode-creator) project. I decided to create this fork due to an unresolved issue and a pending pull request ([PR #13](https://github.com/VittoriDavide/react-native-barcode-creator/pull/13)) that I submitted. Since December 19, 2023, the original issue ([#10](https://github.com/VittoriDavide/react-native-barcode-creator/issues/10)) had not been addressed. Therefore, I published this repository with changes that resolve the problem. Additionally, I performed linting on `src/index.tsx` and `example/src/App.tsx` to improve code quality.

Component to generate QRCode, Code128, PDF417, AZTEC, EAN13 or UPCA natively for react native.

## Screenshots

![alt text](https://randomstuffshared.s3.eu-west-2.amazonaws.com/screenshot.png)

## Installation

```sh
npm install react-native-barcode-creator
```

Go to your ios folder and run:

```sh
pod install
```

## Usage

```js
import BarcodeCreatorViewManager, {
  BarcodeFormat,
} from 'react-native-barcode-creator';

<BarcodeCreatorViewManager
  value={'100'}
  background={'#000000'}
  foregroundColor={'#FFFFFF'}
  format={BarcodeFormat.QR}
  style={styles.box}
/>;
```

## Props

| Prop                  | Description                                                                                                                                                                        | Default            |
| --------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------ |
| **`value`**           | **Mandatory** - The content to add to the Barcode. (EAN-13 should be 13 integers on a string like "5901234123457", UPCA has to be 12 characters "590123412345")                    | _None_             |
| **`encodedValue`**    | Use instead of value, accepts object with base64 and messageEncoded. MessageEncoded only accepts **"ISO-8859-1"**, **"UTF-8"**, **"UTF-16"**. Ex: {base64: "", messageEncoded: ""} | _None_             |
| **`style`**           | Style attributes for the view, as expected in a standard [`View`](https://facebook.github.io/react-native/docs/layout-props.html).                                                 | _None_             |
| **`format`**          | **Mandatory** The format to show in the Barcode, it can be QR, AZTEC, PDF417, CODE128, EAN13 and UPCA.                                                                             | `BarcodeFormat.QR` |
| **`background`**      | The Background Color of the Barcode. (rgba or rgb)                                                                                                                                 | `#FFFFFF`          |
| **`foregroundColor`** | The foreground color to use on the Barcode. (rgba or rgb)                                                                                                                          | `#000000`          |

## Contributing

See the [contributing guide](CONTRIBUTING.md) to learn how to contribute to the repository and the development workflow.

## License

MIT
