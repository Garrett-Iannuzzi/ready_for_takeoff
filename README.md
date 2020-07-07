# ready_for_takeoff

## Overview
- Displays user data to determine account status 

## Project setup
- Run `npm install`
- Run `npm run serve`

## Challenges 
- I got a stuck on the API, I was getting a CORS error so I tried to solve it by creating a config file and setting up a proxy server and changing the header on the request but nothing worked.

## Wins
- I eventually solved the above issue! After reviewing the docs on Vue I had the `created()` method in the wrong place.

## Design Notes 
- My first decision was thinking toward performance speed. I decided between passing along the whole array to each component and then filtering what I needed or filtering on fetch then passing the sorted arrays as props. I opted for the second because that way every time there is a re-render you don't have to re-filter. 
- I also tried creating an accountCard component to render inside each account container to be more dynamic but I was over on time and wanted to get things on the page first. 
- I felt logical to have all three account types as different components since they would be dealing with different information types.
- I decided to create a folder of `layouts` for components that did not deal with any data.

- Overall I would have liked to gone farther but the CORS error stumped me for a while. I have opened issues for the next items I would tackle.
