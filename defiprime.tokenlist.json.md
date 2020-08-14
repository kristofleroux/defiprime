---
permalink: defiprime.tokenlist.json
layout: null
---
{% assign all_projects = site.alternative-savings
| concat: site.analytics
| concat: site.assets-management-tools
| concat: site.assets-tokenization
| concat: site.dao
| concat: site.derivatives
| concat: site.exchanges
| concat: site.infrastructure
| concat: site.insurance
| concat: site.kyc_identity
| concat: site.lending
| concat: site.margin-trading
| concat: site.marketplaces
| concat: site.payments
| concat: site.prediction_markets
| concat: site.stablecoins
 %}
 {
   "name": "My Token List",
   "logoURI": "ipfs://QmUSNbwUxUYNMvMksKypkgWs8unSm8dX2GjCPBVGZ7GGMr",
   "keywords": [
     "audited",
     "verified",
     "special tokens"
   ],
   "tags": {
     "stablecoin": {
       "name": "Stablecoin",
       "description": "Tokens that are fixed to an external asset"
     },
     "compound": {
       "name": "Compound Finance",
       "description": "Tokens that earn interest on compound.finance"
     }
   },
   "timestamp": "2020-06-12T00:00:00+00:00",
   "tokens": [
     {% for all_project in all_projects %}
     {% if all_project.ticker  %}


     {
       "chainId": 1,
       "address": "0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48",
       "symbol": "USDC",
       "name": "{{ all_project.product-title }}",
       "decimals": 6,
       "logoURI": "ipfs://QmXfzKRvjZz3u5JRgC4v5mGVbm9ahrUiB4DgzHBsnWbTMM",
       "tags": [
         "stablecoin"
       ]
     },
     {
       "chainId": 1,
       "address": "0x39AA39c021dfbaE8faC545936693aC917d5E7563",
       "symbol": "cUSDC",
       "name": "Compound USD Coin",
       "decimals": 8,
       "logoURI": "ipfs://QmUSNbwUxUYNMvMksKypkgWs8unSm8dX2GjCPBVGZ7GGMr",
       "tags": [
         "compound"
       ]
     }
   ],
   "version": {
     "major": 1,
     "minor": 0,
     "patch": 0
   }
 }



{% endif %}
 {% endfor %}

 </table>