# App Release Checklist
Everything you need to get your app live on the web and the stores!

So, you've vibe-coded something cool for your phone with [Bolt.new](https://bolt.new). What's next? How do I get this to the app stores? Let's talk about that.

We'll divide this into a few different phases. Take things one step at a time, there's a handful of little and somewhat bigger things to do, but you'll get through them :).

## Tools and accounts you'll need
Get these things in order first to make the rest of the steps go smoothly.

### Grab some tools
_I really like Bolt's Github connection option, so I'll focus on that. but you can also use the Export button and work with the files without connecting them to Github_
- [ ] Create a [Github](https://github.com) account.
- [ ] Download [Github Desktop](https://github.com/apps/desktop) (there's other ways, but Github Desktop is super-easy; just a few clicks and you'll be syncing between Bolt and your desktop)
- [ ] Download [Visual Studio Code](https://code.visualstudio.com/) (you'll use this to edit a few files)
- [ ] Create an [Expo](https://expo.dev) account (you'll use this to build and publish your app)

### Sign up as a developer for the stores
_You'll need accounts with Google and Apple in order to publish to the stores. It can take a little time to get these fully-enabled, so, once you have something you want to publish, sign up for these first_
- [ ] Sign up for the [Apple Developer](https://developer.apple.com/) program ($99 USD/year)
- [ ] Sign up as a [Google Play developer](https://play.google.com/console/u/0/signup) ($25 USD one-time)

## Last mile development and testing
_Once you download your app to your computer and open it in Visual Studio Code, you can complete a few tasks on your way to the stores. Just a few configuration bits, no major coding._

### Web
- [ ] Run `npx expo export --platform web` to build your web project
- [ ] Run `npx eas-cli deploy --prod` to deploy to web.

### Android
- [ ] Run `eas build --profile production --platform android` to build your Play Store-ready app

### iOS
- [ ] Run `npx testflight` to build your iOS app and submit it to the App Store for testing and eventual release

## Prep for the stores

### Screenshots
- [ ] Take at least two screenshots on one of your devices
- [ ] Mock up screenshots for iPhone 16 Pro Max and an Android phone with https://app-mockup.com/
