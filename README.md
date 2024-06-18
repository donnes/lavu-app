# Lavu - Building in Public

Lavu is a Brazilian personal laundry service that connects customers with local, independent laundry professionals. The service aims to provide a convenient and personalized laundry experience by allowing users to schedule pickups and deliveries through their platform. Lavu emphasizes quality, reliability, and customer satisfaction, ensuring that laundry is handled with care and returned clean and fresh. The company supports local economies by partnering with individual laundry providers, offering them a flexible way to earn income.

## Quick Start

To get it running, follow the steps below:

### 1. Setup dependencies

```sh
# Install dependencies
pnpm i

# Configure environment variables
# There is an `.env.example` in the root directory you can use for reference
cp .env.example .env

# Push the Drizzle schema to the database
pnpm db:push
```

### 2. Configure Expo `dev`-script

#### Use iOS Simulator

1. Make sure you have XCode and XCommand Line Tools installed [as shown on expo docs](https://docs.expo.dev/workflow/ios-simulator).

   > **NOTE:** If you just installed XCode, or if you have updated it, you need to open the simulator manually once. Run `npx expo start` from `apps/mobile`, and then enter `I` to launch Expo Go. After the manual launch, you can run `pnpm dev` in the root directory.

   ```diff
   +  "dev": "expo start --ios",
   ```

2. Run `pnpm dev` at the project root folder.

#### Use Android Emulator

1. Install Android Studio tools [as shown on expo docs](https://docs.expo.dev/workflow/android-studio-emulator).

2. Change the `dev` script at `apps/expo/package.json` to open the Android emulator.

   ```diff
   +  "dev": "expo start --android",
   ```

3. Run `pnpm dev` at the project root folder.
