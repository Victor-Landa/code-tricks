Google Analytics
```javascript
module.exports = {
  plugins: [
    {
      resolve: `gatsby-plugin-google-analytics`,
      options: {
          // The property ID; the tracking code won't be generated without it
          trackingId: "UA-89513418-1",
          // Defines where to place the tracking script - `true` in the head and `false` in the body
          head: false,
          // Setting this parameter is optional
          anonymize: true,
          // Setting this parameter is also optional
          respectDNT: true,
          defer: true,
          cookieDomain: "almondcow.co",
          // defaults to false
          enableWebVitalsTracking: true,
      },
    }
  ]
}
```