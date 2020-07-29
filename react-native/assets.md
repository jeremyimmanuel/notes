# Assets

## Custom Fonts

Adding custom fonts to a react native project via react native cli. Check source [here](https://medium.com/@mehrankhandev/ultimate-guide-to-use-custom-fonts-in-react-native-77fcdf859cf4).

```
1. Make assets folder
2. Put .tff files in assets
3. Create `react-native.config.js` file
4. Paste the following code


module.exports = {
  project: {
    ios: {},
    android: {}, // grouped into "project"
  },
  assets: ["./assets/fonts/"], // stays the same
};

5. Run `react-native link` on terminal
6. Use the .tff filename as the font e.g. 

// filename
OpenSans-Bold.ttf

// App.js
fontFamily: "OpenSans-Bold.ttf"
```