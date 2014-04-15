##1 - Introduction

  * Synchronous (OS Folder Analogy)
  * Built on top of Node.js
  * For real-time web apps
  * Shareable Javascript on both sides (server/client)

##2 - Getting Started
  * Packages
    - Core packages
    - Smart packages (37) (install via `meteor add packagename`)
    - Local packages (created by user)
    - Atmosphere smart packages (install via `mrt add packagename`)
    - Npm packages (install via `npm install packagename`)
  * Folder structure (5 folders)
    - `/server`
    - `/client`
    - `/public`
    - `/lib`
    - `/collections`
  * Meteor rules
    - Code in `/server` only runs on the server (same for `/client`)
    - Everything else runs on both sides
    - Files in `/lib` are loaded before anything else
    - Any `main.*` file is loaded after everything else
    - Assets go in `/public`
  * 7 Meteor Principles 
    - Data on the wire: Prefer to send data instead of html
    - One language: Use JavaScript on client and server
    - Database everywhere: Use same db api on client and server
    - Latency compensation: Use prefetching and model simulation to emulate zero-latency
    - Full stack reactivity: Make realtime the default. Use event-driven interfaces
    - Embrace the ecosystem: Open source roots
    - Simplicity equals productivity: Maintain a clean and beautiful code

##2.5 - Deployment
  * 3 Options: Deploy on Meteor subdomain, Modulus, Meteor Up (personal server)
  * Meteor
    - `meteor deploy bolotas-microscope.meteor.com`
  * Modulus
    - `npm install -g modulus` (only first time)
    - `modulus login` (only first time)
    - `modulus project create` (for each project)
    - Create MongoDB database on web interface (for each project)
    - `modulus env set MONGO_URL "mongodb://<user>:<pass>@mongo.onmudulus.net:27817/<database_name>"` (for each project)
    - `modulus deploy`
  * TODO: Meteor Up

##3 - Templates
  * 