# Tomorrow.io Postman Collection
This quickstart is a step-by-step guide that will get you up and running with Postman and the Tomorrow.io [Postman Collection](https://learning.postman.com/docs/postman/collections/intro-to-collections/).

If you are looking for a more in-depth guide and reference for the Tomorrow.io API, please refer to the [Tomorrow.io API documentation](https://docs.tomorrow.io/reference).

![postman-overview](/images/postman.png)

## Getting started
Follow these steps to quickly get started with the [Tomorrow.io API](https://docs.tomorrow.io):

1. [Sign up](https://tomorrow.io/platforms) with Tomorrow.io to get a set of API keys that are required for interacting with the API.
2. Download and install the [Postman app](https://www.getpostman.com/downloads/)
3. Import ["Tomorrow.io Postman Collection"](https://github.com/Tomorrow-IO-API/tomorrow-postman/blob/main/Tomorrow%20Postman%20Collection.json) file or click the button below to install the collection!
4. Import ["Tomorrow.io Production Environment"](https://github.com/Tomorrow-IO-API/tomorrow-postman/blob/main/Tomorrow%20Production%20Environment.json) file and add your `apikey` that you grabbed from our [Development Section](https://app.tomorrow.io)
5. Change the query/path/body parameters by going to the "Pre-request Script" tab and modifying them
6. Click "Send"
  
[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/ab165384adc4cdd1498b?action=collection%2Fimport)

## Collection endpoints
The following collection is a fully-featured set of pre-filled requests that allow you to test the [Tomorrow.io API](https://docs.tomorrow.io/reference), and visualize the responses in a friendly format.
* [Timeline (GET/POST)](https://docs.tomorrow.io/reference/timeline-overview)
* [Events (GET/POST)](https://docs.tomorrow.io/reference/events-overview)
* [Route (POST)](https://docs.tomorrow.io/reference/route-overview)
* [Map › Tile (GET)](https://docs.tomorrow.io/reference/map-overview)
* [Locations](https://docs.tomorrow.io/reference/locations-overview)
* [Insights](https://docs.tomorrow.io/reference/insights-overview)
* [Alerts](https://docs.tomorrow.io/reference/alerts-overview)

## Useful Tools
[JSON to CSV](https://json-csv.com/) can be used to transform a timeline to an CSV - just make sure to flatten the values before using the one-liner js code below and change RESPONSE to the one you got from our API.

```
(RESPONSE).data.timelines[0].intervals.map(obj => Object.assign({}, ...function _flatten(o) { return [].concat(...Object.keys(o).map(k => typeof o[k] === 'object' ? _flatten(o[k]) : ({[k]: o[k]})))}(obj)))
```

[Plotly Chart Studio](https://plotly.com/chart-studio/) can be used to plot the data points. Simply convert a response to .csv (as mentioned above), import, inspect and share.

[Webhook Tester](https://webhook.site/) can be used for receiving webhook calls. Generate a webhook url on this site and use that url in the developers section to get alert notifications.

## Contribute

You can contribute to this project by forking the repo and following the setup steps to import those files. When you've made your contributions in Postman editor, use the File | Export to overwrite the file in your forked branch. Then simply submit the forked branch as a PR back to this repo.
