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

### All
- [ ] If there's any features you can't test in Expo Go, add those and create a [Development Build](https://docs.expo.dev/develop/development-builds/introduction/) to wrap up development.

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

### Optional
- [ ] Consider integrating [EAS Update](https://docs.expo.dev/eas-update/introduction/) so you can make many bugfixes without resubmitting to the stores.

## 3. Get your assets and copy in order
_You'll need a handful of images and some text while filling out your store listing. Let's make them now._

### Screenshots
_Recommendation: Use https://app-mockup.com/ (free) to create the correct sized screenshots with borders/designs, so you can use any device's screenshots when making them_

#### iOS
- [ ] One screenshot matching the size of the iPhone 16 Pro Max (1320 x 2868px)
- [ ] (if targeting iPad) one screenshot matching the 13" iPad (2048 × 2732px)

#### Android
- [ ] Two screenshots with a 9x16 pixel ratio or more vertically (basically any Android phone)

### Others

#### App Store / Play Store
- [ ] Store description
  - Let Bolt or ChatGPT generate this for you!

#### Play Store
- [ ] 512 x 512px version of the icon
  - resize the iOS icon in macOS Preview or MS Paint
- [ ] 1024 x 500px feature graphic
  - Ask ChatGPT to generate one based off your app icon
- [ ] Short description (up to 80 characters)

## 4. Submit to the stores!
_With everything in order, just fill everything out until the App Store and Play Store let you submit!_

### App Store (iOS)
- [ ] Go to [App Store Connect](https://appstoreconnect.apple.com/) to complete the store listing that was automatically created for you
  - [ ] In the main page ("1.0" release), add your screenshots, description, review information, and select the build that was uploaded via `npx testflight`
  - [ ] In **App Information**, set your app name (must be unique), category, and age rating
  - [ ] In **App Privacy**, set your privacy policy URL, indicate any data you collect, and click Publish
- [ ] - [ ] On the main page, click Add for Review to submit!

### Play Store (Android)
- [ ] On the [Play Store Console](https://play.google.com/console), go to the app you created earlier.
- [ ] Start on the **Dashboard** and keep clicking into all the tasks until they're done:
  - [ ] Setup privacy policy, content rating, all the disclosures about news apps, government apps, etc.
  - [ ] Set contact details
  - [ ] Setup store listing (you'll use your screenshots, feature graphic, icon, description, and short description here
  - [ ] At the very bottom of the Dashboard, click on "Select countries and regions" to set app availability
- [ ] Under Test and Release -> Testing -> Internal, choose your release and promote it to Production.
- [ ] Back on Dashboard, submit for review!

## Appendix

### Tools and accounts you'll probably use as you complete these steps

- [ ] Create a [Github](https://github.com) account.
- [ ] Download [Github Desktop](https://github.com/apps/desktop) (there's other ways, but Github Desktop is super-easy; just a few clicks and you'll be syncing between Bolt and your desktop)
- [ ] Download [Visual Studio Code](https://code.visualstudio.com/) (you'll use this to edit a few files)
- [ ] Create an [Expo](https://expo.dev) account (you'll use this to build and publish your app)
