[(https://github.com/user-attachments/assets/e1504aee-3c04-4f8f-9ed2-804d4242be0c)](https://github.com/user-attachments/assets/e1504aee-3c04-4f8f-9ed2-804d4242be0c)
INSTRUCTIONS: There is a .env file that is not gitignored so you should have it in the frontend which
connects it to the backend..

1) Open the app and in the terminal enter: npm install now once that is finished run a new command: cd
backend npm install This should install all dependencies and libraries in frontend and backend. Also
replace tsconfig.json file with:
{
"extends": "expo/tsconfig.base",
"compilerOptions": {
"strict": true,
"jsx": "react-native",
"moduleResolution": "node",
"paths": {
"@/*": ["./*"]
}
},
"include": [
"**/*.ts",
"**/*.tsx",
".expo/types/**/*.ts",
"expo-env.d.ts",
"declarations.d.ts"
]
}

2) In constants/env.ts you'll see something like this: export const API_BASE_URL =
"http://192.168.40.28:5003/"; // Replace with: export const API_BASE_URL =
"https://backend-new-new-167353511624.us-central1.run.app/";

3) If on mac u have to have Xcode installed although it should be installed by default for IOS simulator if
on windows download Android Studio so you can run a android emulator when running the app

4) Now to start the scripts: Open a terminal and run: node backend/dbSetup.js u should get ouputs
knowing that the db is initialized Open a new terminal while the other is running and run: node
backend/server.js u should get outputs that the server has started Open another terminal while both of
those are running and run: npx expo start -c This will start the app and then once it seems like this
command has executed type just 1 letter in this same terminal where u started the app: a (If on windows to
run android simulator) i (If on mac to run ios simulator)
MAKE SURE to acknowledge step 3 or step 4 won’t work

5) To test Doctor: login with username: doctor@example.com password: Doctor@123
To test Admin: login with username: admins@example.com password: Admin@123
