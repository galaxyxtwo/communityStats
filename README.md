# communityStats

## Overview
Share important analytics you collect using [Leto Analytics](https://leto.gg/) with your community! Easily showcase activity data for NFTs, webpages, and more with a static, public stats page (in descending order by view count).

Feel free to use this repo to make your own community stats page!

<img width="1281" alt="Screenshot 2023-10-16 at 12 25 50 PM" src="https://github.com/galaxyxtwo/communityStats/assets/90220293/56b26e1d-c191-4416-b691-68f8c8e76d02">

## Getting Started
Follow the steps below to set up and run the commuityStats React App in development mode:

1. **Clone the Repository**:
  
    ```
    git clone [https://github.com/galaxyxtwo/communityStats]
    cd [communityStats]
2. **Add your CIDs**: 

    This app has an example list of IPFS CIDs in src/app.js. Before launching your app, change these CIDs to the
    production CIDs that you want to display in the leaderboard. 
> **_Note_**: Only IPFS CIDs that have been accessed through the [Leto IPFS Gateway](https://letodev.gitbook.io/getting-started/documentation/ipfs-gateway-api) will return a view count, called "numberAccessed.

3. **Run the Development Server**:
    ```
    npm install
    npm start
    ```

  After executing the above command, the react app should be running in development mode. Navigate to the specified local server address in your browser to view the website.

To run this application in the cloud, choose a hosting provider and then use a cloudflare worker for the api request. Check out the /worker code in this [other example](https://github.com/galaxyxtwo/viewIpfsAnalytics). /worker is Javascript code meant for a Cloudflare worker that processes api requests. /src is the front-end built with React.

## Background

communityStats uses the [Leto Analytics API](https://letodev.gitbook.io/getting-started/documentation/analytics-rest-api) to display a view count for each CID. To make it easy, steps are included to host the communityStats page on IPFS hosting provider, Spheron. This is an awesome IPFS hosting provider, but technically communityStats can be hosted on any cloud provider.

This repo is similar to the viewIpfsAnalytics example, but doesnt include an input box to add CIDs. This allows a developer or community to manage what data is added onto the community webpage. 
    
  Learn more about Leto by visiting the [Leto docs](https://letodev.gitbook.io/getting-started/)!
