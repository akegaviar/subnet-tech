This is a fork of the [original network list by Anton Nell](https://github.com/antonnell/networklist-org).

## Adding a subnet

To add a subnet, fork this repo and add a new object in the `components/chain/subnets.json` file with the details below. Create a PR to merge your change into this repo and it'll automatically go live.

**If you want your project to appear in the projects page, [check also how to add a project](#adding-a-project).**

Subnet attributes details:

```js
{
  "name": "", // chain name
  "chain: "", // used to search
  "title": "", // display name
  "description": "", // optional, max 150 characters
  "projectURL": "", // optional, http URL to the prooject
  "isLive" : true/false // indicates if the subnet is test or live
  "nativeCurrency.name": "", // name of the project token
  "nativeCurrency.symbol": "", // symbol of the project token
  "nativeCurrency.decimals": 18, //
  "chainId": 0x12345 // required for the button to add to metamask. 0x format
  "rpc": "", // RPC endpoint. Required for button to add to metamask
  "blockchain" : "", // optional. provided by Avalanche
  "subnetId" : "", // optional. provided by Avalanche
  "validators": 123 // optional. number of validators
  "faucets": [] // list of urls of different faucets. Maximum 3
  "explorers": []  // list of explorer urls

}
```

## Adding a validator

If you're currently running your own validator and you're open to whitelist someone's subnet, you can create a PR including your details in the `components/validator/validator.json` file as follows:

```js
 {
    "nodeID": "NodeID-xxxxxxx", // your validator node id
    "totalStake": 23496, // amount stacked in the validator
    "feePercentage": 2, // validator fee
    "openToValidate": true, // change to false if you just want to list your validator in the site
    "contactURL": "" // link to a website contact page, discord or telegram

  },
```

**Important**: we do not recommend to include an email address as a contact method to avoid spam.

## Adding a project

If you want to submit your project so it appears in the projects page, create a pull request adding your project information in the `components/project/projects.json` file as follows:

```js
{
    "name": "", // project name
    "description": "",  // project description. One or two phrases
    "logo": "/logos/xxx.jpg", // upload your project logo image to /public/logos/
    "website": "" // project website
  },
```

## Getting Started

This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

First, run the development server:

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.js`. The page auto-updates as you edit the file.

[API routes](https://nextjs.org/docs/api-routes/introduction) can be accessed on [http://localhost:3000/api/hello](http://localhost:3000/api/hello). This endpoint can be edited in `pages/api/hello.js`.

The `pages/api` directory is mapped to `/api/*`. Files in this directory are treated as [API routes](https://nextjs.org/docs/api-routes/introduction) instead of React pages.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.
