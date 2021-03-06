# TypeScript typings for Google Cloud IoT API v1
Registers and manages IoT (Internet of Things) devices that connect to the Google Cloud Platform.

For detailed description please check [documentation](https://cloud.google.com/iot).

## Installing

Install typings for Google Cloud IoT API:
```
npm install @types/gapi.client.cloudiot@v1 --save-dev
```

## Usage

You need to initialize Google API client in your code:
```typescript
gapi.load("client", () => { 
    // now we can use gapi.client
    // ... 
});
```

Then load api client wrapper:
```typescript
gapi.client.load('cloudiot', 'v1', () => {
    // now we can use gapi.client.cloudiot
    // ... 
});
```

Don't forget to authenticate your client before sending any request to resources:
```typescript

// declare client_id registered in Google Developers Console
var client_id = '',
    scope = [     
        // View and manage your data across Google Cloud Platform services
        'https://www.googleapis.com/auth/cloud-platform',
    
        // Register and manage devices in the Google Cloud IoT service
        'https://www.googleapis.com/auth/cloudiot',
    ],
    immediate = true;
// ...

gapi.auth.authorize({ client_id: client_id, scope: scope, immediate: immediate }, authResult => {
    if (authResult && !authResult.error) {
        /* handle succesfull authorization */
    } else {
        /* handle authorization error */
    }
});            
```

After that you can use Google Cloud IoT API resources:

```typescript
```