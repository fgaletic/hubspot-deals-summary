# Deals Summary Card

## Features

- **Deal Summary Display:** Provides key deal details in a compact format.
- **HubSpot CRM Integration:** Uses HubSpot’s CRM Cards API to fetch and display deal data.
- **Serverless Functionality:** Dynamically retrieves and updates deal information.
- **Custom UI Elements:** Designed for an intuitive and seamless user experience within HubSpot.

## Technologies Used

- **HubSpot CRM Cards API**
- **Serverless Functions** (Node.js) *(Note: Serverless functions work well for development and lightweight tasks but may have performance limitations in a live app. Consider using a dedicated backend for high-traffic scenarios.)*
- **React (for UI elements, if applicable)**

- **HubSpot CRM Cards API**
- **Serverless Functions** (Node.js)
- **React (for UI elements, if applicable)**

## Update your CLI & Authenticate Your Account

[Full local environment documentation](https://app.hubspot.com/l/docs/doc/platform/developer-projects-setup#set-up-your-local-environment)

### Step 1: Update Your CLI & Authenticate Your Account

1. Update to the latest CLI version by running:
   ```sh
   npm install -g @hubspot/cli@latest
   ```
2. Run `hs init` to create a config file for your parent account (if you haven’t already done so).
3. Run `hs auth` to authenticate your account. Alternatively, select your pre-authenticated account with:
   ```sh
   hs accounts use
   ```

### Step 2: Create the Project

Run the following command to create a new project:
```sh
hs project create --templateSource="HubSpot/ui-extensions-examples" --dest="deals-summary" --name="deals-summary" --template="deals-summary"
```

### Step 3: Install Dependencies

Change into your project directory and install dependencies:
```sh
cd deals-summary
npm install
```
Run `npm install` in both `/src/app/extensions` and `/src/app/app.functions` directories.

### Step 4: Upload the Project

Run:
```sh
hs project upload
```
To start development mode and see changes reflected locally as you build:
```sh
hs project dev
```

## Test: Create Two Deal Records

1. Navigate to `Sales` > `Deals`.
2. Click `Create deal` and enter a name, amount, and associate it with the `Brian Halligan` contact.
3. Repeat the process to create a second deal.
4. Navigate back to the `Contacts` section and verify that the Deals Summary Card reflects the new deals.

## Setup Local Dev

[Full Local Dev Documentation](https://app.hubspot.com/l/docs/doc/platform/ui-extensions-quickstart#3.-start-local-development)

- Run `npm install` to install dependencies.
- Create a `.env` file inside the `app.functions` directory.
- In your HubSpot account, navigate to `CRM Development` > `Private Apps`, find the Deals Summary App, and copy the access token.
- Add the token to your `.env` file.

Run:
```sh
hs project dev
```
Return to the contact record and refresh the browser. You should see a `Developing locally` icon next to the card title.

## Future Enhancements

- **Average Margin Calculation (Planned):** Currently, the average margin feature is not implemented. Future iterations may include a calculated margin summary.

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss the proposed changes.

## License

MIT License

---

For any questions or support, feel free to reach out!

