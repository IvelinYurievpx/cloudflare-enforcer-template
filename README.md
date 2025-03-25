# CloudFlare Enforcer Template Project

See the full official documentation for the Human Security CloudFlare Enforcer [here](https://docs.humansecurity.com/applications-and-accounts/docs/cloudflare-intro).

## Use case
1. This repo allows you to generate templates for each Human Security CloudFlare Enforcer [Version 5](https://docs.humansecurity.com/applications-and-accounts/docs/cloudflare-intro) (and above).
2. The worker is customized and allows you to:
   * Edit the enforcer configuration in a separate file.
## How to use
1. git clone the project into your working directory.
2. Install dependencies with `npm install`.
3. Configure the enforcer by modifying the `src/config.json` file.
* Under this file you can find 3 types of configuration parameters:
  * **Mandatory** configuration fields that can be found under `Mandatory configurations` comment:   
       * `PX_APP_ID` - The application ID (available in the [portal](https://console.perimeterx.com/))
       * `PX_AUTH_TOKEN` - The server token (available in the [portal](https://console.perimeterx.com/))
       * `PX_COOKIE_SECRET` - The cookie secret associated with the Bot Defender security policy (available in the [portal](https://console.perimeterx.com/))
   * **All other** configuration fields that you can read more about them [here](https://docs.humansecurity.com/applications-and-accounts/docs/configuration-cloudflare):
      *  The simple ones under `Simple function configuration` comment.
      * Custom functions that can be found under `Custom function configurations` comment.
4. Compile the enforcer by running `npm run build` from the project directory.
5. Find the worker file `index.js` in `dist/` folder
