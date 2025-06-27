# App Release Checklist
Everything you need to get your app live on the web and the stores!

So, you've vibe-coded something cool for your phone with [Bolt.new](https://bolt.new). What's next? How do I get this to the app stores? Let's talk about that.

We'll divide this into a few different phases. Take things one step at a time, there's a handful of little and somewhat bigger things to do, but you'll get through them :).

## 1. Finishing Touches to your code in Bolt
_You could technically do these after downloading your project, but might as well do them here, especially the parts that Bolt can generate for you_
- [ ] Create an icon and splash screen image, add them to your project. Follow the guide here: https://docs.expo.dev/develop/user-interface/splash-screen-and-app-icon/
  - Our Figma template (above link) is really helpful for the layout. You can draw your own icon, use tools in Figma, or even ask ChatGPT to generate a logo with a transparent background.
- [ ] Create a Privacy Policy page (URL: `/privacy`)
- [ ] (Optional) Create an `/about` page for your store listing
- [ ] (Optional but recommended) Connect your Bolt project to Github

## 2. Sign up as a developer for the stores
_You'll need accounts with Google and Apple in order to publish to the stores. It can take a little time to get these fully-enabled, so, once you have something you want to publish, sign up for these first_
- [ ] Sign up for the [Apple Developer](https://developer.apple.com/) program ($99 USD/year)
- [ ] Sign up as a [Google Play developer](https://play.google.com/console/u/0/signup) ($25 USD one-time)

## 3. Build and deploy (and test!)
_Download your app to your computer to run the deployment commands (use the file export or Github connection)_

### iOS
- [ ] Run `npx testflight` to build your iOS app and submit it to the App Store for testing and eventual release
  - Check your email to confirm that your app submitted successfully to Testflight
- [ ] Download Testflight, add the code from your email, and test your app

### Android
- [ ] Run `eas build --profile production --platform android` to build your Play Store-ready app
- [ ] Create a store listing at https://play.google.com/console, upload your app to the "Internal" track to start testing, and use the link to install it
  - Another option: use the `preview` build profile to create an APK file you can sideload.

### Web
- [ ] Run `npx expo export --platform web` to build your web project
- [ ] Run `npx eas-cli deploy --prod` to deploy to web.

## 3. Get your image assets in order
_You'll need a handful of images while filling out your store listing. Let's make them now._

### Screenshots
_Recommendation: Use https://app-mockup.com/ (free) to create the correct sized screenshots with borders/designs, so you can use any device's screenshots when making them_

#### iOS
- [ ] One screenshot matching the size of the iPhone 16 Pro Max (1320 x 2868px)
- [ ] (if targeting iPad) one screenshot matching the 13" iPad (2048 × 2732px)

#### Android
- [ ] Two screenshots with a 9x16 pixel ratio or more vertically (basically any Android phone)

### Others

#### Play Store
- [ ] 512 x 512px version of the icon
  - resize the iOS icon in macOS Preview or MS Paint
- [ ] 1024 x 500px feature graphic
  - Ask ChatGPT to generate one based off your app icon

## Appendix

### Tools and accounts you'll probably use as you complete these steps

- [ ] Create a [Github](https://github.com) account.
- [ ] Download [Github Desktop](https://github.com/apps/desktop) (there's other ways, but Github Desktop is super-easy; just a few clicks and you'll be syncing between Bolt and your desktop)
- [ ] Download [Visual Studio Code](https://code.visualstudio.com/) (you'll use this to edit a few files)
- [ ] Create an [Expo](https://expo.dev) account (you'll use this to build and publish your app)
