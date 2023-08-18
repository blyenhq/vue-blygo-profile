# Blygo Button Vue Package

The Blygo Button Package provides integration with the blygo.io SDK for displaying a profile button in your Vue
applications.

## Installation

You can install this package using npm:

```bash
npm install blygo-button-vue
```

## Usage

```vue
<template>
  <div id="app">
    <h1>Vue App with BlygoButton</h1>
    <BlygoButton projectKey="yourProjectKey" email="test@example.com"/>
  </div>
</template>

<script>
import Vue from 'vue';
import BlygoButton from 'blygo-button-vue';

export default {
  components: {
    BlygoButton
  }
};
</script>
```

Replace `yourProjectKey` and `test@example.com` with the appropriate values.

### Props

- `projectKey` - (required): Your Blygo project key. You can find this in your Blygo dashboard.
- `email` - (required): The email address of the user you want to identify in Blygo profile.
- `phone` - (optional): The phone number of the user you want to identify in Blygo profile.
- `title` - (optional): The title of the button. Default is `View Profile`.

## More Information

For more information about the Blygo app and its features, visit [https://blygo.io](https://blygo.io).

## Support

For any issues or questions, please reach out to [support@blygo.io](mailto:support@blygo.io).

## License

This plugin is licensed under the [MIT License](LICENSE.txt).
