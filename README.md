# strapi-s3-cdn

## Configurations

Added cdn url to strapi-provider-upload-s3
**Example**

`./config/plugins.js`

```js
module.exports = ({ env }) => ({
  // ...
  upload: {
    provider: 'aws-s3',
    providerOptions: {
      accessKeyId: env('AWS_ACCESS_KEY_ID'),
      secretAccessKey: env('AWS_ACCESS_SECRET'),
      region: env('AWS_REGION'),
      params: {
        Bucket: env('AWS_BUCKET'),
      },
      cdn: env('CDN_URL') // Hello from the other siiiiiiiiiiide
    },
  },
  // ...
});
```