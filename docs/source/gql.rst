GraphQL
===================================
A preliminary GraphQL API for assets is available at https://gql.instamint.com. Currently, the service searches through staging data only and will point to production data soon.

Asset Query & Schema
-------------------
type Query {
  allAssets: [asset]
  asset(uuid: String): asset
}

type orderbook {
  bidder_name: String
  bidder_id: Float
  best_bid: Float
  ask: String
}

type contract {
  short_name: String
  address: String
  last_used_token_id: Float
  description: String
}

type party {
  owner: String
  client: String
  custodian: String
  issuer: String
}

type asset {
  b2bcross_referenceid: Float
  uuid: String
  created_at: String
  active: Boolean
  ask: String
  best_bid: String
  block_explorerurl: String
  ipfs_meta_dataurl: String
  metadata: String
  mint_completed_status: Boolean
  mint_requestjson: String
  tokenid: Int
  transaction_receiptjson: String
  order_book: orderbook
  contract: contract
  parties: party
  bidder_id: Float
  client_id: Float
  contract_id: Float
  custodian_id: Float
}

