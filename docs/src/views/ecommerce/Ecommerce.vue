<template>
    <div>
      <h1>Demo Ecommerce</h1>
      <p>This is a placeholder component. You can modify or remove it as needed.</p>
    </div>
    <button @click="onClick">Click Me!</button>
  </template>
  
  <script>
  var clevertap = {event:[], profile:[], account:[], onUserLogin:[], notifications:[], privacy:[]};
  // replace with the CLEVERTAP_ACCOUNT_ID with the actual ACCOUNT ID value from your Dashboard -> Settings page
 clevertap.account.push({"id": "W86-KR4-R86Z"});
 clevertap.privacy.push({optOut: false}); //set the flag to true, if the user of the device opts out of sharing their data
 clevertap.privacy.push({useIP: false}); //set the flag to true, if the user agrees to share their IP data
  (function () {
          var wzrk = document.createElement('script');
          wzrk.type = 'text/javascript';
          wzrk.async = true;
          wzrk.src = ('https:' == document.location.protocol ? 'https://d2r1yp2w7bby2u.cloudfront.net' : 'http://static.clevertap.com') + '/js/clevertap.min.js';        
          var s = document.getElementsByTagName('script')[0];
          s.parentNode.insertBefore(wzrk, s);
   })();
  export default {
    name: 'EcommercePage',
    mounted() {
    const uniqueUserId = '227253';
    clevertap.profile.push({
        identity: uniqueUserId,
        name: 'jaya@clevertap.com',
        email: 'ctadmin@clevertap.com'
    });
    },
    methods: {
    onClick() {
      alert('Button clicked!');
      clevertap.event.push("test_event");
    },
  }
  };
  </script>
  
  <style>
  /* Add any custom styles for this component */
  </style>

  