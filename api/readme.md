# GraphQL API
PoC done by following https://www.youtube.com/watch?v=BcZ_ItGplfE

There's something weird happening with the versions, though. Node.js 14 seems to break stuff. This is now running with the workaround from https://stackoverflow.com/questions/59620803/createreadstream-throwing-rangeerror-maximum-call-stack-size-exceeded-when-up meaning adding this part in package.json:
```json
  "resolutions": {
    "fs-capacitor": "^6.2.0",
    "graphql-upload": "^11.0.0"
  }
```
And then running the following:
```bash
npx npm-force-resolutions
npm install
```
There's another discussion about this in https://stackoverflow.com/questions/56423772/unknown-type-upload-in-apollo-server-2-6 but I had no luck with that.
