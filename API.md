      API Definitions                       {"@context":"https://schema.org","@type":"WebPage","description":"Hive Developer Documentation.","headline":"titles.api-def","url":"https://developers.hive.io/apidefinitions/"}

[![Hive Developers logo](/images/logotype_black.svg)](/)
========================================================

 

###### Introduction

*   [Intro to Hive](/#introduction-welcome)
*   [Web2 vs Web3](/#introduction-web3)
*   [Developer workflow](/#introduction-workflow)

###### Getting started

*   [Hive Nodes](/quickstart/#quickstart-hive-full-nodes)
*   [Hive Testnet](/quickstart/#quickstart-testnet)
*   [Accounts](/quickstart/#quickstart-accounts)
*   [Authentication](/quickstart/#quickstart-authentication)
*   [SDK Libraries](/quickstart/#quickstart-choose-library)
*   [Get and Set](/quickstart/#quickstart-fetch-broadcast)

###### JSON-RPC API

*   [Account By Key API](/apidefinitions/#apidefinitions-account-by-key-api)
*   [Account history API](/apidefinitions/#apidefinitions-account-history-api)
*   [Block API](/apidefinitions/#apidefinitions-block-api)
*   [Bridge](/apidefinitions/#apidefinitions-bridge)
*   [Condenser API](/apidefinitions/#apidefinitions-condenser-api)
*   [Database API](/apidefinitions/#apidefinitions-database-api)
*   [Debug Node API](/apidefinitions/#apidefinitions-debug-node-api)
*   [Follow API](/apidefinitions/#apidefinitions-follow-api)
*   [JSON RPC](/apidefinitions/#apidefinitions-jsonrpc)
*   [Market History API](/apidefinitions/#apidefinitions-market-history-api)
*   [Network Broadcast API](/apidefinitions/#apidefinitions-network-broadcast-api)
*   [RC API](/apidefinitions/#apidefinitions-rc-api)
*   [Reputation API](/apidefinitions/#apidefinitions-reputation-api)
*   [Rewards API](/apidefinitions/#apidefinitions-rewards-api)
*   [Tags API](/apidefinitions/#apidefinitions-tags-api)
*   [Transaction Status API](/apidefinitions/#apidefinitions-transaction-status-api)
*   [Wallet Bridge API](/apidefinitions/#apidefinitions-wallet-bridge-api)
*   [Witness API](/apidefinitions/#apidefinitions-witness-api)
*   [Broadcast OPS](/apidefinitions/#apidefinitions-broadcast-ops)
*   [Broadcast OPS Custom](/apidefinitions/#apidefinitions-broadcast-ops-customs)

###### Tutorials

*   [Recipes](/tutorials/#tutorials-recipes)
*   [Javascript](/tutorials/#tutorials-javascript)
*   [Python](/tutorials/#tutorials-python)
*   [PHP](/tutorials/#tutorials-php)
*   [Ruby](/tutorials/#tutorials-ruby)

###### Opportunities

*   [Hive Fund](/services/#services-dhf)
*   [Hive Hackathons](/services/#services-hackathon)
*   [Condenser](/services/#services-hive-blog)
*   [Vision](/services/#services-ecency-com)
*   [ImageHoster](/services/#services-imagehoster)
*   [VideoHoster](/services/#services-videohoster)

[

###### Node Setup

](/nodeop/)

###### Layer 2

*   [Hive Engine](/layer2/#layer2-engine)
*   [HoneyComb](/layer2/#layer2-honeycomb)
*   [VSC](/layer2/#layer2-vsc)

###### Resources

*   [Overview](/resources/#resources-overview)
*   [Whitepaper](/resources/#resources-whitepaper)
*   [Hivesigner](/resources/#resources-hivesigner)
*   [HiveKeychain](/resources/#resources-hive-keychain)
*   [HiveAuth](/resources/#resources-hiveauth)
*   [Jussi](/resources/#resources-jussi)
*   [Tools](/resources/#resources-tools)
*   [Dev support](/resources/#resources-developeradvocate)

###### Glossary

*   [Chain Basics](/glossary/#glossary-chain-basics)
*   [Governance](/glossary/#glossary-governance)
*   [Transactions](/glossary/#glossary-transactions)
*   [API](/glossary/#glossary-api)
*   [Market](/glossary/#glossary-market)

[![](/images/i18n/en.svg)]( /apidefinitions/) [![](/images/i18n/es.svg)](/es/apidefinitions/) [![](/images/i18n/hi.svg)](/hi/apidefinitions/) [![](/images/i18n/de.svg)](/de/apidefinitions/) [![](/images/i18n/fr.svg)](/fr/apidefinitions/) [![](/images/i18n/ru.svg)](/ru/apidefinitions/) [![](/images/i18n/zh.svg)](/zh/apidefinitions/)

Hive Developer Portal - API Definitions
=======================================

![](/images/honey-comb-92.png)

### Account By Key API

Methods:

*   [get\_key\_references](#account_by_key_api.get_key_references)

Used to lookup account information based on a key. **These AppBase API methods are still under development and subject to change.**

*   **Since: HF16**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-key-references)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-key-references)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_key_references)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txaccountupdates2)
    
*   **[Related](/search/?q=get%20key%20references)**

#### account\_by\_key\_api.get\_key\_references[](#account_by_key_api.get_key_references)

Returns all accounts that have the key associated with their owner or active authorities.

##### Query Parameters JSON[](#account_by_key_api.get_key_references-parameter_json)

    {
      "keys": [
        "STM6vJmrwaX5TjgTS9dPH8KsArso5m91fVodJvv91j7G765wqcNM9"
      ]
    }
    

##### Expected Response JSON[](#account_by_key_api.get_key_references-expected_response_json)

    {"accounts": ["hiveio"]}
    

##### Example `curl`[](#account_by_key_api.get_key_references-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"account_by_key_api.get_key_references", "params":{"keys":["STM6vJmrwaX5TjgTS9dPH8KsArso5m91fVodJvv91j7G765wqcNM9"]}, "id":1}' https://api.hive.blog
    

* * *

### Account history API

Methods:

*   [enum\_virtual\_ops](#account_history_api.enum_virtual_ops)
*   [get\_account\_history](#account_history_api.get_account_history)
*   [get\_ops\_in\_block](#account_history_api.get_ops_in_block)
*   [get\_transaction](#account_history_api.get_transaction)

Used to lookup account history information. **These AppBase API methods are still under development and subject to change.**

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-account-history)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-account-history)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_account_history)
    
*   **[Related](/search/?q=get%20account%20history)**

#### account\_history\_api.get\_account\_history[](#account_history_api.get_account_history)

Returns a history of all operations for a given account. Parameters:

*   `account:string`
*   `start:int`. e.g.: -1 for reverse history or any positive numeric
*   `limit:int` up to 1000
*   `include_reversible:boolean` (optional) If set to true also operations from reversible block will be included
*   `operation_filter_low:int` (optional)
*   `operation_filter_high:int` (optional)

If either `operation_filter_low` or `operation_filter_high` are set, the set of returned operations will include only these matching bitwise filter.

For the first 64 operations (as defined in [protocol/operations.hpp](https://gitlab.syncad.com/hive/hive/-/blob/master/libraries/protocol/include/hive/protocol/operations.hpp)), set the corresponding bit in `operation_filter_low`; for the higher-numbered operations, set the bit in operation\_filter\_high (pretending operation\_filter is a 128-bit bitmask composed of `{operation_filter_high, operation_filter_low}`)

`account` (string)

`start` (int)

`limit` (int)

`include_reversible` (boolean)

`operation_filter_low` (int)

`operation_filter_high` (int)

 

`"hiveio"`

`1000`

`1000`

 

 

 

Queries the account named `hiveio` starting on the latest item in history, up to 1,000 results.

`"alice"`

`-1`

`1000`

 

 

 

Queries the account named `alice` starting on the oldest item in history, up to 1,000 results.

`"bob"`

`-1`

`1000`

true

1

 

Queries **only votes** by the account named `bob` starting on the oldest item in history, up to 1,000 results.

`"charlie"`

`-1`

`1000`

true

262144

 

Queries **only custom jsons** by the account named `charlie` starting on the oldest item in history, up to 1,000 results.

`"emma"`

`-1`

`1000`

true

0

1

Queries **only proposal payments** to the account named `emma` starting on the oldest item in history, up to 1,000 results.

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#account_history_apiget_account_history)

##### Query Parameters JSON[](#account_history_api.get_account_history-parameter_json)

    {
      "account": "",
      "start": "18446744073709551615",
      "limit": 1000,
      "include_reversible": true,
      "operation_filter_low": 4294967295,
      "operation_filter_high": 4294967295
    }
    

##### Expected Response JSON[](#account_history_api.get_account_history-expected_response_json)

    {
      "history": [
        [
          99,
          {
            "trx_id": "0000000000000000000000000000000000000000",
            "block": 0,
            "trx_in_block": 4294967295,
            "op_in_trx": 0,
            "virtual_op": 0,
            "timestamp": "2019-12-09T21:32:39",
            "op": {}
          }
        ]
      ]
    }
    

##### Example `curl`[](#account_history_api.get_account_history-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"account_history_api.get_account_history", "params":{"account":"hiveio", "start":1000, "limit":1000}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"account_history_api.get_account_history", "params":{"account":"hiveio", "start":-1, "limit":1000}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"account_history_api.get_account_history", "params":{"account":"bob", "start":-1, "limit":1000, "include_reversible": true, "operation_filter_low": 1}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"account_history_api.get_account_history", "params":{"account":"charlie", "start":-1, "limit":1000, "include_reversible": true, "operation_filter_low": 262144}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"account_history_api.get_account_history", "params":{"account":"emma", "start":-1, "limit":1000, "include_reversible": true, "operation_filter_low": 0, "operation_filter_high": 1}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-ops-in-block)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-ops-in-block)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_ops_in_block)
    
*   **[Related](/search/?q=get%20ops%20block)**

#### account\_history\_api.get\_ops\_in\_block[](#account_history_api.get_ops_in_block)

Returns all operations contained in a block. Parameter:

*   `block_num:int`
*   `only_virtual:boolean`
*   `include_reversible:boolean` (optional) If set to true also operations from reversible block will be included if block\_num points to such block.

##### Query Parameters JSON[](#account_history_api.get_ops_in_block-parameter_json)

    {
      "block_num": 0,
      "only_virtual": false,
      "include_reversible": true
    }
    

##### Expected Response JSON[](#account_history_api.get_ops_in_block-expected_response_json)

    {
      "ops": [
        {
          "trx_id": "0000000000000000000000000000000000000000",
          "block": 0,
          "trx_in_block": 4294967295,
          "op_in_trx": 0,
          "virtual_op": 0,
          "timestamp": "2019-10-06T09:05:15",
          "op": {}
        }
      ]
    }
    

##### Example `curl`[](#account_history_api.get_ops_in_block-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"account_history_api.get_ops_in_block", "params":{"block_num":1,"only_virtual":false}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"account_history_api.get_ops_in_block", "params":{"block_num":5443322,"only_virtual":true}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"account_history_api.get_ops_in_block", "params":{"block_num":5443322,"only_virtual":true,"include_reversible":true}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-transaction)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-transaction)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_transaction)
    
    [hivesql](https://docs.hivesql.io/technical-informations/database-diagram#blocks-and-transactions)
    
*   **[Related](/search/?q=get%20transaction)**

#### account\_history\_api.get\_transaction[](#account_history_api.get_transaction)

Returns the details of a transaction based on a transaction id (including their signatures, operations like also a block\_num it was included to).

*   `id:string` trx\_id of expected transaction
*   `include_reversible:boolean` (optional) If set to true also operations from reversible block will be included if block\_num points to such block.

##### Query Parameters JSON[](#account_history_api.get_transaction-parameter_json)

    {"id": "6fde0190a97835ea6d9e651293e90c89911f933c"}
    

##### Expected Response JSON[](#account_history_api.get_transaction-expected_response_json)

    {
      "jsonrpc": "2.0",
      "result": {
        "ref_block_num": 36374,
        "ref_block_prefix": 3218139339,
        "expiration": "2018-04-09T00:29:06",
        "operations": [
          {
            "type": "claim_reward_balance_operation",
            "value": {
              "account": "social",
              "reward_hive": {
                "amount": "0",
                "precision": 3,
                "nai": "@@000000021"
              },
              "reward_hbd": {
                "amount": "0",
                "precision": 3,
                "nai": "@@000000013"
              },
              "reward_vests": {
                "amount": "1",
                "precision": 6,
                "nai": "@@000000037"
              }
            }
          }
        ],
        "extensions": [],
        "signatures": [
          "1b01bdbb0c0d43db821c09ae8a82881c1ce3ba0eca35f23bc06541eca05560742f210a21243e20d04d5c88cb977abf2d75cc088db0fff2ca9fdf2cba753cf69844"
        ],
        "transaction_id": "6fde0190a97835ea6d9e651293e90c89911f933c",
        "block_num": 21401130,
        "transaction_num": 25
      },
      "id": 1
    }
    

##### Example `curl`[](#account_history_api.get_transaction-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"account_history_api.get_transaction", "params":{"id":"6fde0190a97835ea6d9e651293e90c89911f933c"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"account_history_api.get_transaction", "params":{"id":"6fde0190a97835ea6d9e651293e90c89911f933c", "include_reversible": true}, "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF24**
*   **SDK Reference**
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations)
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=enum_virtual_ops)
    
*   **[Related](/search/?q=enum%20virtual%20ops)**

#### account\_history\_api.enum\_virtual\_ops[](#account_history_api.enum_virtual_ops)

Allows to specify range of blocks to retrieve virtual operations for.

*   `block_range_begin:int` starting block number (inclusive) to search for virtual operations
*   `block_range_end:int` last block number (exclusive) to search for virtual operations
*   `include_reversible:boolean` (optional) If set to true also operations from reversible block will be included if block\_num points to such block.
*   `group_by_block` (optional) true/false
*   `operation_begin` (optional) starting virtual operation in given block (inclusive)
*   `limit` (optional) a limit of retrieved operations
*   `filter` (optional) a filter that decides which an operation matches - used bitwise filtering equals to position such as:
    *   `fill_convert_request_operation = 0x000001`
    *   `author_reward_operation = 0x000002`
    *   `curation_reward_operation = 0x000004`
    *   `comment_reward_operation = 0x000008`
    *   `liquidity_reward_operation = 0x000010`
    *   `interest_operation = 0x000020`
    *   `fill_vesting_withdraw_operation = 0x000040`
    *   `fill_order_operation = 0x000080`
    *   `shutdown_witness_operation = 0x000100`
    *   `fill_transfer_from_savings_operation = 0x000200`
    *   `hardfork_operation = 0x000400`
    *   `comment_payout_update_operation = 0x000800`
    *   `return_vesting_delegation_operation = 0x001000`
    *   `comment_benefactor_reward_operation = 0x002000`
    *   `producer_reward_operation = 0x004000`
    *   `clear_null_account_balance_operation = 0x008000`
    *   `proposal_pay_operation = 0x010000`
    *   `sps_fund_operation = 0x020000`
    *   `hardfork_hive_operation = 0x040000`
    *   `hardfork_hive_restore_operation = 0x080000`
    *   `delayed_voting_operation = 0x100000`
    *   `consolidate_treasury_balance_operation = 0x200000`
    *   `effective_comment_vote_operation = 0x400000`
    *   `ineffective_delete_comment_operation = 0x800000`
    *   `sps_convert_operation = 0x1000000`
    *   `dhf_funding_operation = 0x0020000`
    *   `dhf_conversion_operation = 0x1000000`
    *   `expired_account_notification_operation = 0x2000000`
    *   `changed_recovery_account_operation = 0x4000000`
    *   `transfer_to_vesting_completed_operation = 0x8000000`
    *   `pow_reward_operation = 0x10000000`
    *   `vesting_shares_split_operation = 0x20000000`
    *   `account_created_operation = 0x40000000`
    *   `fill_collateralized_convert_request_operation = 0x80000000`
    *   `system_warning_operation = 0x100000000`
    *   `fill_recurrent_transfer_operation = 0x200000000`
    *   `failed_recurrent_transfer_operation = 0x400000000`
    *   `limit_order_cancelled_operation = 0x800000000`
    *   `producer_missed_operation = 0x1000000000`
    *   `proposal_fee_operation = 0x2000000000`
    *   `collateralized_convert_immediate_conversion_operation = 0x4000000000`
    *   `escrow_approved_operation = 0x8000000000`
    *   `escrow_rejected_operation = 0x10000000000`
    *   `proxy_cleared_operation = 0x20000000000`

##### Query Parameters JSON[](#account_history_api.enum_virtual_ops-parameter_json)

    {
      "block_range_begin": 1,
      "block_range_end": 2,
      "include_reversible": true,
      "group_by_block": false,
      "operation_begin": 0,
      "limit": 1000,
      "filter": 1
    }
    

##### Expected Response JSON[](#account_history_api.enum_virtual_ops-expected_response_json)

    {
      "ops": [
        {
          "trx_id": "0000000000000000000000000000000000000000",
          "block": 0,
          "trx_in_block": 4294967295,
          "op_in_trx": 0,
          "virtual_op": 0,
          "timestamp": "2016-03-24T17:46:30",
          "op": {},
          "operation_id": "18446744069414584320"
        }
      ]
    }
    

##### Example `curl`[](#account_history_api.enum_virtual_ops-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"account_history_api.enum_virtual_ops", "params":{"block_range_begin":1,"block_range_end":2}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"account_history_api.enum_virtual_ops", "params":{"block_range_begin":1,"block_range_end":2,"include_reversible":true}, "id":1}' https://api.hive.blog
    

* * *

### Block API

Methods:

*   [get\_block](#block_api.get_block)
*   [get\_block\_header](#block_api.get_block_header)
*   [get\_block\_range](#block_api.get_block_range)

Used to query values related to the block plugin. **These AppBase API methods are still under development and subject to change.**

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-block)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-block)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/BlockApi)
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_block)
    
*   **[Related](/search/?q=get%20block)**

#### block\_api.get\_block[](#block_api.get_block)

Retrieve a full, signed block of the referenced block, or null if no matching block was found.

**Parameters:**

*   `block_num:int`

`block_num` (int)

 

`1`

Queries the very first block.

`8675309`

Queries block number 8,675,309.

`62396745`

Queries block number 62,396,745.

##### Query Parameters JSON[](#block_api.get_block-parameter_json)

    {"block_num": 0}
    

##### Expected Response JSON[](#block_api.get_block-expected_response_json)

    {
      "block": {
        "previous": "0000000000000000000000000000000000000000",
        "timestamp": "2016-03-24T16:05:00",
        "witness": "",
        "transaction_merkle_root": "0000000000000000000000000000000000000000",
        "extensions": [],
        "witness_signature": "",
        "transactions": [],
        "block_id": "",
        "signing_key": "",
        "transaction_ids": []
      }
    }
    

##### Example `curl`[](#block_api.get_block-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"block_api.get_block", "params":{"block_num":1}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"block_api.get_block", "params":{"block_num":8675309}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"block_api.get_block", "params":{"block_num":62396745}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-block-header)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-block-header)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/BlockApi)
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_block_header)
    
*   **[Related](/search/?q=get%20block%20header)**

#### block\_api.get\_block\_header[](#block_api.get_block_header)

Retrieve a block header of the referenced block, or null if no matching block was found.

**Parameters:**

*   `block_num:int` - Height of the block whose header should be returned

`block_num` (int)

 

`1`

Queries the block headers for the very first block.

`8675309`

Queries block headers for block number 8,675,309.

`62396745`

Queries block headers for block number 62,396,745.

##### Query Parameters JSON[](#block_api.get_block_header-parameter_json)

    {"block_num": 0}
    

##### Expected Response JSON[](#block_api.get_block_header-expected_response_json)

    {
      "header": {
        "previous": "0000000000000000000000000000000000000000",
        "timestamp": "2016-03-24T16:05:00",
        "witness": "",
        "transaction_merkle_root": "0000000000000000000000000000000000000000",
        "extensions": []
      }
    }
    

##### Example `curl`[](#block_api.get_block_header-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"block_api.get_block_header", "params":{"block_num":1}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"block_api.get_block_header", "params":{"block_num":8675309}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"block_api.get_block_header", "params":{"block_num":62396745}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_block_range)
    
*   **[Related](/search/?q=get%20block%20range)**

#### block\_api.get\_block\_range[](#block_api.get_block_range)

Retrieve a range of full, signed blocks. The list may be shorter than requested if `count` blocks would take you past the current head block.

**Parameters:**

*   `starting_block_num` - Height of the first block to be returned
*   `count` - the maximum number of blocks to return

`starting_block_num` (int)

`count` (int)

 

`1`

`10`

Queries the block headers for the very first block through the tenth block.

`8675309`

`50`

Queries block headers for block numbers 8,675,309 through 8,675,359.

`62396745`

`1000`

Queries block headers for block numbers 62,396,745 through 62,397,745.

See: [!149](https://gitlab.syncad.com/hive/hive/-/merge_requests/149), [702ea4a](https://gitlab.syncad.com/hive/hive/-/commit/702ea4a758a98b4d164a616dadb34683d40e7af4)

##### Query Parameters JSON[](#block_api.get_block_range-parameter_json)

    {"starting_block_num": 0, "count": 0}
    

##### Expected Response JSON[](#block_api.get_block_range-expected_response_json)

    {"blocks": []}
    

##### Example `curl`[](#block_api.get_block_range-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"block_api.get_block_range", "params":{"starting_block_num": 1, "count": 10}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"block_api.get_block_range", "params":{"starting_block_num": 8675309, "count": 50}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"block_api.get_block_range", "params":{"starting_block_num": 62396745, "count": 1000}, "id":1}' https://api.hive.blog
    

* * *

### Bridge

Methods:

*   [account\_notifications](#bridge.account_notifications)
*   [does\_user\_follow\_any\_lists](#bridge.does_user_follow_any_lists)
*   [get\_account\_posts](#bridge.get_account_posts)
*   [get\_community](#bridge.get_community)
*   [get\_community\_context](#bridge.get_community_context)
*   [get\_discussion](#bridge.get_discussion)
*   [get\_follow\_list](#bridge.get_follow_list)
*   [get\_payout\_stats](#bridge.get_payout_stats)
*   [get\_post](#bridge.get_post)
*   [get\_post\_header](#bridge.get_post_header)
*   [get\_profile](#bridge.get_profile)
*   [get\_ranked\_posts](#bridge.get_ranked_posts)
*   [get\_relationship\_between\_accounts](#bridge.get_relationship_between_accounts)
*   [list\_all\_subscriptions](#bridge.list_all_subscriptions)
*   [list\_communities](#bridge.list_communities)
*   [list\_community\_roles](#bridge.list_community_roles)
*   [list\_pop\_communities](#bridge.list_pop_communities)
*   [list\_subscribers](#bridge.list_subscribers)

Presents data interpreted by the hivemind database as JSON-RPC.

Also see: [Communities Broadcast Ops](/apidefinitions/#apidefinitions-broadcast-ops-communities)

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_ranked_posts)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/tags)
    
*   **[Related](/search/?q=get%20ranked%20posts)**

#### bridge.get\_ranked\_posts[](#bridge.get_ranked_posts)

Get ranked posts.

Supported values for `sort`:

*   `trending`
*   `hot`
*   `created`
*   `promoted`
*   `payout`
*   `payout_comments`
*   `muted`

The value for `tag` can be any valid tag.

The value for `observer` can be any valid account or empty string.

##### Query Parameters JSON[](#bridge.get_ranked_posts-parameter_json)

    {"sort": "", "tag": "", "observer": ""}
    

##### Expected Response JSON[](#bridge.get_ranked_posts-expected_response_json)

    [
      {
        "post_id": 12345678,
        "author": "alice",
        "permlink": "that-march-hare",
        "category": "wonderland",
        "title": "That March Hare",
        "body": "I think he went mad.",
        "json_metadata": {
          "tags": ["wonderland"],
          "app": "hiveblog/0.1"
        },
        "created": "2019-12-05T16:29:12",
        "updated": "2019-12-05T16:29:12",
        "depth": 0,
        "children": 0,
        "net_rshares": 1539574839484,
        "is_paidout": false,
        "payout_at": "2019-12-12T16:29:12",
        "payout": 0.286,
        "pending_payout_value": "0.286 HBD",
        "author_payout_value": "0.000 HBD",
        "curator_payout_value": "0.000 HBD",
        "promoted": "0.000 HBD",
        "replies": [],
        "active_votes": [{"voter": "bob", "rshares": "67759296290"}],
        "author_reputation": 47.15,
        "stats": {
          "hide": false,
          "gray": false,
          "total_votes": 12,
          "flag_weight": 0
        },
        "beneficiaries": [],
        "max_accepted_payout": "1000000.000 HBD",
        "percent_hbd": 10000,
        "url": "/wonderland/@alice/that-march-hare",
        "blacklists": []
      }
    ]
    

##### Example `curl`[](#bridge.get_ranked_posts-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"bridge.get_ranked_posts", "params":{"sort":"trending","tag":"","observer":"alice"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=account_notifications)
    
    [openApi](https://gitlab.syncad.com/hive/hivemind/-/blob/pczempiel_openapi_bridge/openApi/client/docs/DefaultApi.md#bridge_account_notifications)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Bridge)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/followers)
    
*   **[Related](/search/?q=account%20notifications)**

#### bridge.account\_notifications[](#bridge.account_notifications)

Account notifications.

Supported values for `type`:

*   `new_community` - a new community was created
*   `set_role` - mod/admin adds a role to an account
*   `set_props` - properties set for a community
*   `set_label` - a title/badge/label has been set for an account
*   `mute_post` - a post has been muted, with a reason
*   `unmute_post` - a post has been unmuted, with a reason
*   `pin_post` - a post has been pinned
*   `unpin_post` - a post has been unpinned
*   `flag_post` - a post has been flagged by a member, with a reason
*   `error` - provides feedback to developers for ops that cannot be interpreted
*   `subscribe` - an account has subscribed to a community
*   `reply` - a post has been replied to
*   `reblog` - a post has been reblogged/reblogged
*   `follow` - an account has followed another account
*   `mention` - author mentions an account
*   `vote` - voter votes for an author

The `score` value is based on the originating account’s rank.

##### Query Parameters JSON[](#bridge.account_notifications-parameter_json)

    {"account": "alice", "limit": 100}
    

##### Expected Response JSON[](#bridge.account_notifications-expected_response_json)

    [
      {
        "id": 3629306,
        "type": "vote",
        "score": 25,
        "date": "2019-11-20T07:48:06",
        "msg": "@bob voted on your post ($0.013)",
        "url": "@alice/a-post-by-alice"
      }
    ]
    

##### Example `curl`[](#bridge.account_notifications-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"bridge.account_notifications", "params":{"account":"alice","limit":100}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=does_user_follow_any_lists)
    
    [openApi](https://gitlab.syncad.com/hive/hivemind/-/blob/pczempiel_openapi_bridge/openApi/client/docs/DefaultApi.md#bridge_does_user_follow_any_lists)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Bridge)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/blacklistsfollows)
    
*   **[Related](/search/?q=user%20follow%20lists)**

#### bridge.does\_user\_follow\_any\_lists[](#bridge.does_user_follow_any_lists)

Checks if a given observer follows any blacklists or mute lists.

##### Query Parameters JSON[](#bridge.does_user_follow_any_lists-parameter_json)

    {"observer": "alice"}
    

##### Expected Response JSON[](#bridge.does_user_follow_any_lists-expected_response_json)

    false
    

##### Example `curl`[](#bridge.does_user_follow_any_lists-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"bridge.does_user_follow_any_lists", "params":{"observer":"alice"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_account_posts)
    
    [openApi](https://gitlab.syncad.com/hive/hivemind/-/blob/pczempiel_openapi_bridge/openApi/client/docs/DefaultApi.md#bridge_get_account_posts)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Bridge)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/reblogs)
    
*   **[Related](/search/?q=get%20account%20posts)**

#### bridge.get\_account\_posts[](#bridge.get_account_posts)

Lists posts related to a given account.

*   `sort` - Supported values:
    *   `blog` - top posts authored by given account (excluding posts to communities - unless explicitely reblogged) plus reblogs ranked by creation/reblog time
    *   `feed` - top posts from blogs of accounts that given account is following ranked by creation/reblog time, not older than last month
    *   `posts` - op posts authored by given account, newer first comments - replies authored by given account, newer first
    *   `replies` - replies to posts of given account, newer first
    *   `payout` - all posts authored by given account that were not yet cashed out
*   `account`: account name, points to valid account
*   `start_author`: author account name, if passed must be passed with `start_permlink` \[optional\]
*   `start_permlink`: post permlink of given author, point to valid post, paging mechanism \[optional\]
*   `limit`: if omitted the server will use the default value of 20 \[optional\]
*   `observer`: ignored for `blog`, feed and `replies`, otherwise when passed has to point to valid account used to fill blacklist stats and mark posts of authors blacklisted by observer, at this time ignored \[optional\]

##### Query Parameters JSON[](#bridge.get_account_posts-parameter_json)

    {"sort": "blog", "account": "alice", "limit": 1}
    

##### Expected Response JSON[](#bridge.get_account_posts-expected_response_json)

    [
      {
        "post_id": 101867403,
        "author": "hiveio",
        "permlink": "around-the-hive-reflections",
        "category": "hiveecosystem",
        "title": "Around the Hive: Reflections",
        "body": "It's been a busy year so far for developers on Hive. Layer 2 solutions are in progress, key optimization is an ongoing priority ...",
        "json_metadata": {
          "tags": ["hiveecosystem"],
          "users": ["blocktrades", "howo"],
          "image": [
            "https://images.hive.blog/768x0/https://files.peakd.com/file/peakd-hive/hiveio/pKjrNcbK-Hive-Wallpaper-1920x1080.png",
            "https://images.hive.blog/DQmR3iwCn9yvwXDXfuNjmMX6FrjAvFfYQWgA4QRckpens1j/hive%20dividers-02.png"
          ],
          "links": [
            "https://gitlab.syncad.com/hive/hive-whitepaper/-/blob/master/technical-vision/infographic.pdf"
          ],
          "app": "hiveblog/0.1",
          "format": "markdown",
          "description": "The strength of Hive lies in our decentralization."
        },
        "created": "2021-02-14T08:16:03",
        "updated": "2021-02-14T08:16:03",
        "depth": 0,
        "children": 15,
        "net_rshares": 93531156115025,
        "is_paidout": true,
        "payout_at": "2021-02-21T08:16:03",
        "payout": 0,
        "pending_payout_value": "0.000 HBD",
        "author_payout_value": "0.000 HBD",
        "curator_payout_value": "0.000 HBD",
        "promoted": "0.000 HBD",
        "replies": [],
        "author_reputation": 69.29,
        "stats": {
          "hide": false,
          "gray": false,
          "total_votes": 129,
          "flag_weight": 0
        },
        "url": "/hiveecosystem/@hiveio/around-the-hive-reflections",
        "beneficiaries": [],
        "max_accepted_payout": "0.000 HBD",
        "percent_hbd": 10000,
        "active_votes": [],
        "blacklists": []
      }
    ]
    

##### Example `curl`[](#bridge.get_account_posts-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"bridge.get_account_posts", "params":{"sort":"blog", "account": "alice", "limit": 1}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_community_context)
    
    [openApi](https://gitlab.syncad.com/hive/hivemind/-/blob/pczempiel_openapi_bridge/openApi/client/docs/DefaultApi.md#bridge_get_community_context)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Bridge)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/communities)
    
*   **[Related](/search/?q=get%20community%20context)**

#### bridge.get\_community\_context[](#bridge.get_community_context)

Gets the role, subscription status, and title for a given account in a given community.

##### Query Parameters JSON[](#bridge.get_community_context-parameter_json)

    {"name": "hive-111111", "account": "therealwolf"}
    

##### Expected Response JSON[](#bridge.get_community_context-expected_response_json)

    {
      "role": "admin",
      "subscribed": true,
      "title": "Witness: @therealwolf"
    }
    

##### Example `curl`[](#bridge.get_community_context-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"bridge.get_community_context", "params":{"name": "hive-111111", "account": "therealwolf"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_discussion)
    
    [openApi](https://gitlab.syncad.com/hive/hivemind/-/blob/pczempiel_openapi_bridge/openApi/client/docs/DefaultApi.md#bridge_get_discussion)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Bridge)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/tags)
    
*   **[Related](/search/?q=get%20discussion)**

#### bridge.get\_discussion[](#bridge.get_discussion)

Gives a flattened discussion tree starting at given post.

##### Query Parameters JSON[](#bridge.get_discussion-parameter_json)

    {
      "author": "hiveio",
      "permlink": "around-the-hive-reflections",
      "observer": "alice"
    }
    

##### Expected Response JSON[](#bridge.get_discussion-expected_response_json)

    {
      "hiveio/around-the-hive-reflections": {
        "post_id": 101867403,
        "author": "hiveio",
        "permlink": "around-the-hive-reflections",
        "category": "hiveecosystem",
        "title": "Around the Hive: Reflections",
        "body": "It's been a busy year so far for developers on Hive. Layer 2 solutions are in progress, key optimization is an ongoing priority ...",
        "json_metadata": {
          "tags": ["hiveecosystem"],
          "users": ["blocktrades", "howo"],
          "image": [
            "https://images.hive.blog/768x0/https://files.peakd.com/file/peakd-hive/hiveio/pKjrNcbK-Hive-Wallpaper-1920x1080.png",
            "https://images.hive.blog/DQmR3iwCn9yvwXDXfuNjmMX6FrjAvFfYQWgA4QRckpens1j/hive%20dividers-02.png"
          ],
          "links": [
            "https://gitlab.syncad.com/hive/hive-whitepaper/-/blob/master/technical-vision/infographic.pdf"
          ],
          "app": "hiveblog/0.1",
          "format": "markdown",
          "description": "The strength of Hive lies in our decentralization."
        },
        "created": "2021-02-14T08:16:03",
        "updated": "2021-02-14T08:16:03",
        "depth": 0,
        "children": 15,
        "net_rshares": 93531156115025,
        "is_paidout": true,
        "payout_at": "2021-02-21T08:16:03",
        "payout": 0,
        "pending_payout_value": "0.000 HBD",
        "author_payout_value": "0.000 HBD",
        "curator_payout_value": "0.000 HBD",
        "promoted": "0.000 HBD",
        "replies": [],
        "author_reputation": 69.29,
        "stats": {
          "hide": false,
          "gray": false,
          "total_votes": 129,
          "flag_weight": 0
        },
        "url": "/hiveecosystem/@hiveio/around-the-hive-reflections",
        "beneficiaries": [],
        "max_accepted_payout": "0.000 HBD",
        "percent_hbd": 10000,
        "active_votes": [],
        "blacklists": []
      }
    }
    

##### Example `curl`[](#bridge.get_discussion-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"bridge.get_discussion", "params":{"author": "hiveio", "permlink": "around-the-hive-reflections", "observer": "alice"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_follow_list)
    
    [openApi](https://gitlab.syncad.com/hive/hivemind/-/blob/pczempiel_openapi_bridge/openApi/client/docs/DefaultApi.md#bridge_get_follow_list)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Bridge)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/followers)
    
*   **[Related](/search/?q=get%20follow%20list)**

#### bridge.get\_follow\_list[](#bridge.get_follow_list)

Returns blacklisted/muted accounts or list of blacklists/mute lists followed by a given observer.

*   `observer` - valid account
*   `follow_type` - Supported values:
    *   `follow_blacklist`
    *   `follow_muted`
    *   `blacklisted`
    *   `muted`

##### Query Parameters JSON[](#bridge.get_follow_list-parameter_json)

    {
      "observer": "blocktrades",
      "follow_type": "follow_blacklist"
    }
    

##### Expected Response JSON[](#bridge.get_follow_list-expected_response_json)

    [
      {
        "name": "hive.blog",
        "blacklist_description": "",
        "muted_list_description": ""
      }
    ]
    

##### Example `curl`[](#bridge.get_follow_list-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"bridge.get_follow_list", "params":{"observer": "blocktrades", "follow_type": "follow_blacklist"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_profile)
    
    [openApi](https://gitlab.syncad.com/hive/hivemind/-/blob/pczempiel_openapi_bridge/openApi/client/docs/DefaultApi.md#bridge_get_profile)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Bridge)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/accounts)
    
*   **[Related](/search/?q=get%20profile)**

#### bridge.get\_profile[](#bridge.get_profile)

Gets profile

*   `account` - valid account
*   `observer` - valid account \[optional\]

##### Query Parameters JSON[](#bridge.get_profile-parameter_json)

    {"account": "alice", "observer": "bob"}
    

##### Expected Response JSON[](#bridge.get_profile-expected_response_json)

    {
      "id": 241,
      "name": "alice",
      "created": "2016-03-25T15:09:27",
      "active": "2016-04-29T22:28:00",
      "post_count": 0,
      "reputation": 25,
      "blacklists": [],
      "stats": {"rank": 0, "following": 0, "followers": 431},
      "metadata": {
        "profile": {
          "name": "",
          "about": "",
          "website": "",
          "location": "",
          "cover_image": "",
          "profile_image": "",
          "blacklist_description": "",
          "muted_list_description": ""
        }
      },
      "context": {"followed": false}
    }
    

##### Example `curl`[](#bridge.get_profile-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"bridge.get_profile", "params":{"account": "alice", "observer": "bob"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=list_communities)
    
    [openApi](https://gitlab.syncad.com/hive/hivemind/-/blob/pczempiel_openapi_bridge/openApi/client/docs/DefaultApi.md#bridge_list_communities)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Bridge)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/communities)
    
*   **[Related](/search/?q=list%20communities)**

#### bridge.list\_communities[](#bridge.list_communities)

Gets community

*   `last` - name of community; paging mechanism \[optional\]
*   `limit` - limit number of listed communities, default: `100` \[optional\]
*   `query` - filters against `title` and `about` community fields \[optional\]
*   `sort` - default: `rank` \[optional\]
    *   `rank` - sort by community rank
    *   `new` - sort by newest community
    *   `subs` - sort by subscriptions
*   `observer` - a valid account \[optional\]

##### Query Parameters JSON[](#bridge.list_communities-parameter_json)

    {"limit": 1, "query": "wall street bets"}
    

##### Expected Response JSON[](#bridge.list_communities-expected_response_json)

    [
      {
        "id": 1432978,
        "name": "hive-103566",
        "title": "Wall Street Bets",
        "about": "Wall Street Bets - In Case Reddit Shuts Down.",
        "lang": "en",
        "type_id": 1,
        "is_nsfw": false,
        "subscribers": 6,
        "sum_pending": 0,
        "num_pending": 0,
        "num_authors": 0,
        "created_at": "2021-01-28 18:34:09",
        "avatar_url": "",
        "context": {},
        "admins": ["spitr"]
      }
    ]
    

##### Example `curl`[](#bridge.list_communities-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"bridge.list_communities", "params":{"limit": 1, "query": "wall street bets"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=list_pop_communities)
    
    [openApi](https://gitlab.syncad.com/hive/hivemind/-/blob/pczempiel_openapi_bridge/openApi/client/docs/DefaultApi.md#bridge_list_pop_communities)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Bridge)
    
*   **[Related](/search/?q=list%20pop%20communities)**

#### bridge.list\_pop\_communities[](#bridge.list_pop_communities)

Gets a list of popular communities.

*   `limit` - limit number of listed communities, default: `25` \[optional\]

##### Query Parameters JSON[](#bridge.list_pop_communities-parameter_json)

    {"limit": 10}
    

##### Expected Response JSON[](#bridge.list_pop_communities-expected_response_json)

    [
      ["hive-167922", "LeoFinance"],
      ["hive-194913", "Photography Lovers"],
      ["hive-148441", "GEMS"],
      ["hive-196037", "DTube"],
      ["hive-196708", "Hive Pets"],
      ["hive-120586", "Foodies Bee Hive"],
      ["hive-140217", "Hive Gaming"],
      ["hive-174578", "OCD"],
      ["hive-129496", "Nerday"],
      ["hive-193816", "Music"]
    ]
    

##### Example `curl`[](#bridge.list_pop_communities-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"bridge.list_pop_communities", "params":{"limit": 10}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=list_subscribers)
    
    [openApi](https://gitlab.syncad.com/hive/hivemind/-/blob/pczempiel_openapi_bridge/openApi/client/docs/DefaultApi.md#bridge_list_subscribers)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Bridge)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/communitiessubscribers)
    
*   **[Related](/search/?q=list%20subscribers)**

#### bridge.list\_subscribers[](#bridge.list_subscribers)

Gets a list of subscribers for a given community.

*   `community` - community category name
*   `last` - name of subscriber; paging mechanism \[optional\]
*   `limit` - limit number of listed subscribers, default: `100` \[optional\]

##### Query Parameters JSON[](#bridge.list_subscribers-parameter_json)

    {"community": "hive-111111", "limit": 10}
    

##### Expected Response JSON[](#bridge.list_subscribers-expected_response_json)

    [
      [
        "gatticus",
        "guest",
        null,
        "2021-02-18 13:15:42"
      ],
      [
        "thewarkettle",
        "guest",
        null,
        "2021-02-15 22:04:36"
      ],
      [
        "darkflame",
        "guest",
        null,
        "2021-02-14 00:30:12"
      ],
      [
        "oiuygtfrd76543",
        "guest",
        null,
        "2021-02-01 19:35:03"
      ],
      ["bhattg", "guest", null, "2021-02-01 18:39:06"],
      [
        "elenahornfilm",
        "guest",
        null,
        "2021-02-01 09:19:54"
      ],
      [
        "mrhappypants",
        "guest",
        null,
        "2021-02-01 01:03:48"
      ],
      [
        "petrahaller",
        "guest",
        null,
        "2021-02-01 00:08:09"
      ],
      [
        "hgregoria",
        "guest",
        null,
        "2021-01-29 18:46:12"
      ],
      [
        "theblockabout",
        "guest",
        null,
        "2021-01-29 15:21:48"
      ]
    ]
    

##### Example `curl`[](#bridge.list_subscribers-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"bridge.list_subscribers", "params":{"community": "hive-111111", "limit": 10}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=list_community_roles)
    
    [openApi](https://gitlab.syncad.com/hive/hivemind/-/blob/pczempiel_openapi_bridge/openApi/client/docs/DefaultApi.md#bridge_list_community_roles)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Bridge)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/communitiesroles)
    
*   **[Related](/search/?q=list%20community%20roles)**

#### bridge.list\_community\_roles[](#bridge.list_community_roles)

List community roles and labels for each account in the community.

*   `community` - community category name
*   `last` - name of subscriber; paging mechanism \[optional\]
*   `limit` - limit number of listed subscribers, default: `100` \[optional\]

##### Query Parameters JSON[](#bridge.list_community_roles-parameter_json)

    {"community": "hive-123456"}
    

##### Expected Response JSON[](#bridge.list_community_roles-expected_response_json)

    [
      ["hive-123456", "owner", ""],
      ["alice", "admin", "Miss"]
    ]
    

##### Example `curl`[](#bridge.list_community_roles-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"bridge.list_community_roles", "params":{"community":"hive-123456"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=list_all_subscriptions)
    
    [openApi](https://gitlab.syncad.com/hive/hivemind/-/blob/pczempiel_openapi_bridge/openApi/client/docs/DefaultApi.md#bridge_list_all_subscriptions)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Bridge)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/communitiessubscribers)
    
*   **[Related](/search/?q=list%20subscriptions)**

#### bridge.list\_all\_subscriptions[](#bridge.list_all_subscriptions)

List all subscriptions, titles, and roles to a community for an account.

*   `account`: account name, points to valid account

##### Query Parameters JSON[](#bridge.list_all_subscriptions-parameter_json)

    {"account": "alice"}
    

##### Expected Response JSON[](#bridge.list_all_subscriptions-expected_response_json)

    [
      ["hive-123456", "Wonderland", "guest", ""],
      [
        "hive-654321",
        "Tulgey Wood",
        "admin",
        "Mrs. Vex"
      ]
    ]
    

##### Example `curl`[](#bridge.list_all_subscriptions-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"bridge.list_all_subscriptions", "params":{"account":"alice"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_community)
    
    [openApi](https://gitlab.syncad.com/hive/hivemind/-/blob/pczempiel_openapi_bridge/openApi/client/docs/DefaultApi.md#bridge_get_community)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Bridge)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/communities)
    
*   **[Related](/search/?q=get%20community)**

#### bridge.get\_community[](#bridge.get_community)

Get community details.

*   `name` - community category name
*   `observer` - valid account \[optional\]

##### Query Parameters JSON[](#bridge.get_community-parameter_json)

    {"name": "hive-123456", "observer": "alice"}
    

##### Expected Response JSON[](#bridge.get_community-expected_response_json)

    {
      "id": 1332149,
      "name": "hive-123456",
      "title": "@hive-123456",
      "about": "Wonderland",
      "lang": "en",
      "type_id": 1,
      "is_nsfw": false,
      "subscribers": 0,
      "sum_pending": 0,
      "num_pending": 0,
      "num_authors": 0,
      "created_at": "2019-10-27 08:28:54",
      "context": {
        "role": "admin",
        "title": "Miss",
        "subscribed": true
      },
      "avatar_url": "",
      "description": "",
      "flag_text": "",
      "settings": {},
      "team": [
        ["hive-123456", "owner", ""],
        ["alice", "admin", "Miss"]
      ]
    }
    

##### Example `curl`[](#bridge.get_community-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"bridge.get_community", "params":{"name":"hive-123456","observer":"alice"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_relationship_between_accounts)
    
    [openApi](https://gitlab.syncad.com/hive/hivemind/-/blob/pczempiel_openapi_bridge/openApi/client/docs/DefaultApi.md#bridge_get_relationship_between_accounts)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Bridge)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/blacklists)
    
*   **[Related](/search/?q=get%20relationship%20accounts)**

#### bridge.get\_relationship\_between\_accounts[](#bridge.get_relationship_between_accounts)

Tells what relations connect given accounts from the perspective of first account.

##### Query Parameters JSON[](#bridge.get_relationship_between_accounts-parameter_json)

    ["alice", "bob"]
    

##### Expected Response JSON[](#bridge.get_relationship_between_accounts-expected_response_json)

    {
      "follows": false,
      "ignores": false,
      "blacklists": false,
      "follows_blacklists": false,
      "follows_muted": false
    }
    

##### Example `curl`[](#bridge.get_relationship_between_accounts-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"bridge.get_relationship_between_accounts", "params":["alice", "bob"], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_payout_stats)
    
    [openApi](https://gitlab.syncad.com/hive/hivemind/-/blob/pczempiel_openapi_bridge/openApi/client/docs/DefaultApi.md#bridge_get_payout_stats)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Bridge)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/comments)
    
*   **[Related](/search/?q=get%20payout%20stats)**

#### bridge.get\_payout\_stats[](#bridge.get_payout_stats)

Lists communities ordered by payout with stats (total payout, number of posts and authors).

*   `limit` - if omitted the server will use the default value of 250 \[optional\]

##### Query Parameters JSON[](#bridge.get_payout_stats-parameter_json)

    {"limit": 250}
    

##### Expected Response JSON[](#bridge.get_payout_stats-expected_response_json)

    {
      "items": [
        [
          "hive-167922",
          "LeoFinance",
          10881.39,
          16791,
          1466
        ]
      ],
      "total": 107662.592,
      "blogs": 14453.794
    }
    

##### Example `curl`[](#bridge.get_payout_stats-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"bridge.get_payout_stats", "params":{"limit": 1}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"bridge.get_payout_stats", "params":{"limit": 250}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_post)
    
    [openApi](https://gitlab.syncad.com/hive/hivemind/-/blob/pczempiel_openapi_bridge/openApi/client/docs/DefaultApi.md#bridge_get_post)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Bridge)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/comments)
    
*   **[Related](/search/?q=get%20post)**

#### bridge.get\_post[](#bridge.get_post)

Gives single selected post.

*   `author` - valid account
*   `permlink` - valid permlink
*   `observer` - valid account \[optional\]

##### Query Parameters JSON[](#bridge.get_post-parameter_json)

    {
      "author": "hiveio",
      "permlink": "around-the-hive-reflections"
    }
    

##### Expected Response JSON[](#bridge.get_post-expected_response_json)

    {
      "post_id": 101867403,
      "author": "hiveio",
      "permlink": "around-the-hive-reflections",
      "category": "hiveecosystem",
      "title": "Around the Hive: Reflections",
      "body": "It's been a busy year so far for developers on Hive. Layer 2 solutions are in progress, key optimization is an ongoing priority ...",
      "json_metadata": {
        "tags": ["hiveecosystem"],
        "users": ["blocktrades", "howo"],
        "image": [
          "https://images.hive.blog/768x0/https://files.peakd.com/file/peakd-hive/hiveio/pKjrNcbK-Hive-Wallpaper-1920x1080.png",
          "https://images.hive.blog/DQmR3iwCn9yvwXDXfuNjmMX6FrjAvFfYQWgA4QRckpens1j/hive%20dividers-02.png"
        ],
        "links": [
          "https://gitlab.syncad.com/hive/hive-whitepaper/-/blob/master/technical-vision/infographic.pdf"
        ],
        "app": "hiveblog/0.1",
        "format": "markdown",
        "description": "The strength of Hive lies in our decentralization."
      },
      "created": "2021-02-14T08:16:03",
      "updated": "2021-02-14T08:16:03",
      "depth": 0,
      "children": 15,
      "net_rshares": 93531156115025,
      "is_paidout": true,
      "payout_at": "2021-02-21T08:16:03",
      "payout": 0,
      "pending_payout_value": "0.000 HBD",
      "author_payout_value": "0.000 HBD",
      "curator_payout_value": "0.000 HBD",
      "promoted": "0.000 HBD",
      "replies": [],
      "author_reputation": 69.29,
      "stats": {
        "hide": false,
        "gray": false,
        "total_votes": 129,
        "flag_weight": 0
      },
      "url": "/hiveecosystem/@hiveio/around-the-hive-reflections",
      "beneficiaries": [],
      "max_accepted_payout": "0.000 HBD",
      "percent_hbd": 10000,
      "active_votes": [],
      "blacklists": []
    }
    

##### Example `curl`[](#bridge.get_post-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"bridge.get_post", "params":{"author": "alice", "permlink": "that-march-hare", "observer": "bob"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"bridge.get_post", "params":{"author": "hiveio", "permlink": "around-the-hive-reflections"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_post_header)
    
    [openApi](https://gitlab.syncad.com/hive/hivemind/-/blob/pczempiel_openapi_bridge/openApi/client/docs/DefaultApi.md#bridge_post_header)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Bridge)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/comments)
    
*   **[Related](/search/?q=get%20post%20header)**

#### bridge.get\_post\_header[](#bridge.get_post_header)

Gives very basic information on given post.

*   `author` - valid account
*   `permlink` - valid permlink

##### Query Parameters JSON[](#bridge.get_post_header-parameter_json)

    {
      "author": "hiveio",
      "permlink": "around-the-hive-reflections"
    }
    

##### Expected Response JSON[](#bridge.get_post_header-expected_response_json)

    {
      "author": "hiveio",
      "permlink": "around-the-hive-reflections",
      "category": "hiveecosystem",
      "depth": 0
    }
    

##### Example `curl`[](#bridge.get_post_header-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"bridge.get_post_header", "params":{"author": "alice", "permlink": "that-march-hare"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"bridge.get_post_header", "params":{"author": "hiveio", "permlink": "around-the-hive-reflections"}, "id":1}' https://api.hive.blog
    

* * *

### Condenser API

Methods:

*   [broadcast\_transaction](#condenser_api.broadcast_transaction)
*   [broadcast\_transaction\_synchronous](#condenser_api.broadcast_transaction_synchronous)
*   [find\_proposals](#condenser_api.find_proposals)
*   [find\_rc\_accounts](#condenser_api.find_rc_accounts)
*   [find\_recurrent\_transfers](#condenser_api.find_recurrent_transfers)
*   [get\_account\_count](#condenser_api.get_account_count)
*   [get\_account\_history](#condenser_api.get_account_history)
*   [get\_account\_reputations](#condenser_api.get_account_reputations)
*   [get\_accounts](#condenser_api.get_accounts)
*   [get\_active\_votes](#condenser_api.get_active_votes)
*   [get\_active\_witnesses](#condenser_api.get_active_witnesses)
*   [get\_block](#condenser_api.get_block)
*   [get\_block\_header](#condenser_api.get_block_header)
*   [get\_blog](#condenser_api.get_blog)
*   [get\_blog\_authors](#condenser_api.get_blog_authors)
*   [get\_blog\_entries](#condenser_api.get_blog_entries)
*   [get\_chain\_properties](#condenser_api.get_chain_properties)
*   [get\_collateralized\_conversion\_requests](#condenser_api.get_collateralized_conversion_requests)
*   [get\_comment\_discussions\_by\_payout](#condenser_api.get_comment_discussions_by_payout)
*   [get\_config](#condenser_api.get_config)
*   [get\_content](#condenser_api.get_content)
*   [get\_content\_replies](#condenser_api.get_content_replies)
*   [get\_conversion\_requests](#condenser_api.get_conversion_requests)
*   [get\_current\_median\_history\_price](#condenser_api.get_current_median_history_price)
*   [get\_discussions\_by\_author\_before\_date](#condenser_api.get_discussions_by_author_before_date)
*   [get\_dynamic\_global\_properties](#condenser_api.get_dynamic_global_properties)
*   [get\_escrow](#condenser_api.get_escrow)
*   [get\_expiring\_vesting\_delegations](#condenser_api.get_expiring_vesting_delegations)
*   [get\_feed\_history](#condenser_api.get_feed_history)
*   [get\_follow\_count](#condenser_api.get_follow_count)
*   [get\_followers](#condenser_api.get_followers)
*   [get\_following](#condenser_api.get_following)
*   [get\_hardfork\_version](#condenser_api.get_hardfork_version)
*   [get\_key\_references](#condenser_api.get_key_references)
*   [get\_market\_history](#condenser_api.get_market_history)
*   [get\_market\_history\_buckets](#condenser_api.get_market_history_buckets)
*   [get\_next\_scheduled\_hardfork](#condenser_api.get_next_scheduled_hardfork)
*   [get\_open\_orders](#condenser_api.get_open_orders)
*   [get\_ops\_in\_block](#condenser_api.get_ops_in_block)
*   [get\_order\_book](#condenser_api.get_order_book)
*   [get\_owner\_history](#condenser_api.get_owner_history)
*   [get\_potential\_signatures](#condenser_api.get_potential_signatures)
*   [get\_reblogged\_by](#condenser_api.get_reblogged_by)
*   [get\_recent\_trades](#condenser_api.get_recent_trades)
*   [get\_recovery\_request](#condenser_api.get_recovery_request)
*   [get\_required\_signatures](#condenser_api.get_required_signatures)
*   [get\_reward\_fund](#condenser_api.get_reward_fund)
*   [get\_savings\_withdraw\_from](#condenser_api.get_savings_withdraw_from)
*   [get\_savings\_withdraw\_to](#condenser_api.get_savings_withdraw_to)
*   [get\_ticker](#condenser_api.get_ticker)
*   [get\_trade\_history](#condenser_api.get_trade_history)
*   [get\_transaction](#condenser_api.get_transaction)
*   [get\_transaction\_hex](#condenser_api.get_transaction_hex)
*   [get\_trending\_tags](#condenser_api.get_trending_tags)
*   [get\_version](#condenser_api.get_version)
*   [get\_vesting\_delegations](#condenser_api.get_vesting_delegations)
*   [get\_volume](#condenser_api.get_volume)
*   [get\_withdraw\_routes](#condenser_api.get_withdraw_routes)
*   [get\_witness\_by\_account](#condenser_api.get_witness_by_account)
*   [get\_witness\_count](#condenser_api.get_witness_count)
*   [get\_witness\_schedule](#condenser_api.get_witness_schedule)
*   [get\_witnesses](#condenser_api.get_witnesses)
*   [get\_witnesses\_by\_vote](#condenser_api.get_witnesses_by_vote)
*   [is\_known\_transaction](#condenser_api.is_known_transaction)
*   [list\_proposal\_votes](#condenser_api.list_proposal_votes)
*   [list\_proposals](#condenser_api.list_proposals)
*   [list\_rc\_accounts](#condenser_api.list_rc_accounts)
*   [list\_rc\_direct\_delegations](#condenser_api.list_rc_direct_delegations)
*   [lookup\_account\_names](#condenser_api.lookup_account_names)
*   [lookup\_accounts](#condenser_api.lookup_accounts)
*   [lookup\_witness\_accounts](#condenser_api.lookup_witness_accounts)
*   [verify\_authority](#condenser_api.verify_authority)

To help with this transition, we created `condenser_api`, which contains all of the API methods that currently exist and uses the existing argument formatting. The easiest way to get your app to work with Appbase is to change the api to `condenser_api`.

All calls in `condenser_api` will return `[]` as the argument, as the array argument passing is opaque and implemented in the API calls themselves. They follow the current argument formatting. Existing apps should only need to skip using login\_api and send all of their calls to condenser\_api without any other changes required to use Appbase.

For example, calling `get_dynamic_global_properties` with `condenser_api` vs `database_api`:

    {"jsonrpc":"2.0", "method":"condenser_api.get_dynamic_global_properties", "params":[], "id":1}
    

    {"jsonrpc":"2.0", "method":"database_api.get_dynamic_global_properties", "id":1}
    

Because the method has no arguments, the params field can be omitted when not using `condenser_api`. However, it can optionally be included as the void type (e.g. `"params":{}`) but it is not required.

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#broadcast-api)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#broadcast-transaction)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=broadcast%20transaction)**

#### condenser\_api.broadcast\_transaction[](#condenser_api.broadcast_transaction)

Used to broadcast a transaction.

Also see: [network\_broadcast\_api.broadcast\_transaction](/apidefinitions/#network_broadcast_api.broadcast_transaction)

##### Query Parameters JSON[](#condenser_api.broadcast_transaction-parameter_json)

    [
      {
        "ref_block_num": 0,
        "ref_block_prefix": 0,
        "expiration": "1970-01-01T00:00:00",
        "operations": [],
        "extensions": [],
        "signatures": []
      }
    ]
    

##### Expected Response JSON[](#condenser_api.broadcast_transaction-expected_response_json)

    {}
    

##### Example `curl`[](#condenser_api.broadcast_transaction-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.broadcast_transaction", "params":[{"ref_block_num":1097,"ref_block_prefix":2181793527,"expiration":"2016-03-24T18:00:21","operations":[["vote",{"voter":"hiveio","author":"alice","permlink":"a-post-by-alice","weight":10000}]],"extensions":[],"signatures":[]}], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.broadcast_transaction", "params":[{"ref_block_num":1097,"ref_block_prefix":2181793527,"expiration":"2016-03-24T18:00:21","operations":[["pow",{"worker_account":"cloop3","block_id":"00000449f7860b82b4fbe2f317c670e9f01d6d9a","nonce":3899,"work":{"worker":"STM7P5TDnA87Pj9T4mf6YHrhzjC1KbPZpNxLWCcVcHxNYXakpoT4F","input":"ae8e7c677119d22385f8c48026fee7aad7bba693bf788d7f27047f40b47738c0","signature":"1f38fe9a3f9989f84bd94aa5bbc88beaf09b67f825aa4450cf5105d111149ba6db560b582c7dbb026c7fc9c2eb5051815a72b17f6896ed59d3851d9a0f9883ca7a","work":"000e7b209d58f2e64b36e9bf12b999c6c7af168cc3fc41eb7f8a4bf796c174c3"},"props":{"account_creation_fee":{"amount":"100000","precision":3,"nai":"@@000000021"},"maximum_block_size":131072,"hbd_interest_rate":1000}}]],"extensions":[],"signatures":[]}], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#broadcast-api)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/TransactionBuilder)
    
*   **[Related](/search/?q=broadcast%20transaction%20synchronous)**

#### condenser\_api.broadcast\_transaction\_synchronous[](#condenser_api.broadcast_transaction_synchronous)

Used to broadcast a transaction and waits for it to be processed synchronously.

##### Query Parameters JSON[](#condenser_api.broadcast_transaction_synchronous-parameter_json)

    [
      {
        "ref_block_num": 0,
        "ref_block_prefix": 0,
        "expiration": "1970-01-01T00:00:00",
        "operations": [],
        "extensions": [],
        "signatures": []
      }
    ]
    

##### Expected Response JSON[](#condenser_api.broadcast_transaction_synchronous-expected_response_json)

    {
      "id": "0000000000000000000000000000000000000000",
      "block_num": 0,
      "trx_num": 0,
      "expired": false
    }
    

##### Example `curl`[](#condenser_api.broadcast_transaction_synchronous-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.broadcast_transaction_synchronous", "params":[{"ref_block_num":1097,"ref_block_prefix":2181793527,"expiration":"2016-03-24T18:00:21","operations":[["vote",{"voter":"hiveio","author":"alice","permlink":"a-post-by-alice","weight":10000}]],"extensions":[],"signatures":[]}], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.broadcast_transaction_synchronous", "params":[{"ref_block_num":1097,"ref_block_prefix":2181793527,"expiration":"2016-03-24T18:00:21","operations":[["pow",{"worker_account":"cloop3","block_id":"00000449f7860b82b4fbe2f317c670e9f01d6d9a","nonce":3899,"work":{"worker":"STM7P5TDnA87Pj9T4mf6YHrhzjC1KbPZpNxLWCcVcHxNYXakpoT4F","input":"ae8e7c677119d22385f8c48026fee7aad7bba693bf788d7f27047f40b47738c0","signature":"1f38fe9a3f9989f84bd94aa5bbc88beaf09b67f825aa4450cf5105d111149ba6db560b582c7dbb026c7fc9c2eb5051815a72b17f6896ed59d3851d9a0f9883ca7a","work":"000e7b209d58f2e64b36e9bf12b999c6c7af168cc3fc41eb7f8a4bf796c174c3"},"props":{"account_creation_fee":{"amount":"10000","precision":3,"nai":"@@000000021"},"maximum_block_size":131072,"hbd_interest_rate":1000}}]],"extensions":[],"signatures":[]}], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_account_count)
    
*   **[Related](/search/?q=get%20account%20count)**

#### condenser\_api.get\_account\_count[](#condenser_api.get_account_count)

Returns the number of accounts.

##### Query Parameters JSON[](#condenser_api.get_account_count-parameter_json)

    []
    

##### Expected Response JSON[](#condenser_api.get_account_count-expected_response_json)

    0
    

##### Example `curl`[](#condenser_api.get_account_count-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_account_count", "params":[], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_account_history)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-account-history)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-account-history)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/followers)
    
*   **[Related](/search/?q=get%20account%20history)**

#### condenser\_api.get\_account\_history[](#condenser_api.get_account_history)

Returns a history of all operations for a given account. Parameters:

*   `account:string`
*   `start:int`. e.g.: -1 for reverse history or any positive numeric
*   `limit:int` up to 1000
*   `operation_filter_low:int` (optional)
*   `operation_filter_high:int` (optional)

If either `operation_filter_low` or `operation_filter_high` are set, the set of returned operations will include only these matching bitwise filter.

For the first 64 operations (as defined in [protocol/operations.hpp](https://gitlab.syncad.com/hive/hive/-/blob/master/libraries/protocol/include/hive/protocol/operations.hpp)), set the corresponding bit in `operation_filter_low`; for the higher-numbered operations, set the bit in operation\_filter\_high (pretending operation\_filter is a 128-bit bitmask composed of `{operation_filter_high, operation_filter_low}`)

`account` (string)

`start` (int)

`limit` (int)

`operation_filter_low` (int)

`operation_filter_low` (int)

 

`"hiveio"`

`1000`

`1000`

 

 

Queries the account named `hiveio` starting on the latest item in history, up to 1,000 results.

`"alice"`

`-1`

`1000`

 

 

Queries the account named `alice` starting on the oldest item in history, up to 1,000 results.

`"bob"`

`-1`

`1000`

1

 

Queries **only votes** by the account named `bob` starting on the oldest item in history, up to 1,000 results.

`"charlie"`

`-1`

`1000`

262144

 

Queries **only custom jsons** by the account named `charlie` starting on the oldest item in history, up to 1,000 results.

`"emma"`

`-1`

`1000`

0

1

Queries **only proposal payments** by the account named `emma` starting on the oldest item in history, up to 1,000 results.

Also see: [account\_history\_api.get\_account\_history](/apidefinitions/#account_history_api.get_account_history), [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#condenser_apiget_account_history)

##### Query Parameters JSON[](#condenser_api.get_account_history-parameter_json)

    ["", 0, 1000]
    

##### Expected Response JSON[](#condenser_api.get_account_history-expected_response_json)

    [
      99,
      {
        "trx_id": "0000000000000000000000000000000000000000",
        "block": 0,
        "trx_in_block": 4294967295,
        "op_in_trx": 0,
        "virtual_op": 0,
        "timestamp": "2019-12-09T21:32:39",
        "op": {}
      }
    ]
    

##### Example `curl`[](#condenser_api.get_account_history-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_account_history", "params":["hiveio", 1000, 1000], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_account_history", "params":["hiveio", -1, 1000], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_account_history", "params":["bob", -1, 1000, 1], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_account_history", "params":["charlie", -1, 1000, 262144], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_account_history", "params":["emma", -1, 1000, 0, 1], "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF13**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_account_reputations)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-account-reputations)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-account-reputations)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20account%20reputations)**

#### condenser\_api.get\_account\_reputations[](#condenser_api.get_account_reputations)

Returns a list of account reputations. Parameters: `account_lower_bound:string`; `limit:int` up to 1000

`account_lower_bound` (string)

`limit` (int)

 

`"hiveio"`

`1`

Queries for accounts that start with “hiveio”, only one result.

`"a"`

`10`

Queries for accounts that start with “a”, up to 10 results.

Also see: [follow\_api.get\_account\_reputations](/apidefinitions/#follow_api.get_account_reputations)

##### Query Parameters JSON[](#condenser_api.get_account_reputations-parameter_json)

    ["", 1000]
    

##### Expected Response JSON[](#condenser_api.get_account_reputations-expected_response_json)

    []
    

##### Example `curl`[](#condenser_api.get_account_reputations-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_account_reputations", "params":["hiveio", 1], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_account_reputations", "params":["a", 10], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_accounts)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-accounts)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.blockchain.html#beem.blockchain.Blockchain.get_all_accounts)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/accounts)
    
*   **[Related](/search/?q=get%20accounts)**

#### condenser\_api.get\_accounts[](#condenser_api.get_accounts)

Returns accounts, queried by name. Parameters: `account:string array`; `delayed_votes_active:boolean`

`account` (string array)

`delayed_votes_active` (boolean)

 

`["hiveio"]`

 

Queries for account named “hiveio”.

`["hiveio", "alice"]`

false

Queries for accounts named “hiveio” and “alice” with `delayed_votes` hidden.

Also see: [database\_api.find\_accounts](/apidefinitions/#database_api.find_accounts)

##### Query Parameters JSON[](#condenser_api.get_accounts-parameter_json)

    [[""]]
    

##### Expected Response JSON[](#condenser_api.get_accounts-expected_response_json)

    {
      "id": 1370484,
      "name": "hiveio",
      "owner": {
        "weight_threshold": 1,
        "account_auths": [],
        "key_auths": [
          [
            "STM65PUAPA4yC4RgPtGgsPupxT6yJtMhmT5JHFdsT3uoCbR8WJ25s",
            1
          ]
        ]
      },
      "active": {
        "weight_threshold": 1,
        "account_auths": [],
        "key_auths": [
          [
            "STM69zfrFGnZtU3gWFWpQJ6GhND1nz7TJsKBTjcWfebS1JzBEweQy",
            1
          ]
        ]
      },
      "posting": {
        "weight_threshold": 1,
        "account_auths": [["threespeak", 1], ["vimm.app", 1]],
        "key_auths": [
          [
            "STM6vJmrwaX5TjgTS9dPH8KsArso5m91fVodJvv91j7G765wqcNM9",
            1
          ]
        ]
      },
      "memo_key": "STM7wrsg1BZogeK7X3eG4ivxmLaH69FomR8rLkBbepb3z3hm5SbXu",
      "json_metadata": "",
      "posting_json_metadata": "{\"profile\":{\"pinned\":\"none\",\"version\":2,\"website\":\"hive.io\",\"profile_image\":\"https://files.peakd.com/file/peakd-hive/hiveio/Jp2YHc6Q-hive-logo.png\",\"cover_image\":\"https://files.peakd.com/file/peakd-hive/hiveio/Xe1TcEBi-hive-banner.png\"}}",
      "proxy": "",
      "last_owner_update": "1970-01-01T00:00:00",
      "last_account_update": "2020-11-12T01:20:48",
      "created": "2020-03-06T12:22:48",
      "mined": false,
      "recovery_account": "steempeak",
      "last_account_recovery": "1970-01-01T00:00:00",
      "reset_account": "null",
      "comment_count": 0,
      "lifetime_vote_count": 0,
      "post_count": 31,
      "can_vote": true,
      "voting_manabar": {
        "current_mana": "598442432741",
        "last_update_time": 1591297380
      },
      "downvote_manabar": {
        "current_mana": "149610608184",
        "last_update_time": 1591297380
      },
      "voting_power": 0,
      "balance": "11.682 HIVE",
      "savings_balance": "0.000 HIVE",
      "hbd_balance": "43.575 HBD",
      "hbd_seconds": "0",
      "hbd_seconds_last_update": "2020-10-21T02:45:12",
      "hbd_last_interest_payment": "2020-10-21T02:45:12",
      "savings_hbd_balance": "0.000 HBD",
      "savings_hbd_seconds": "0",
      "savings_hbd_seconds_last_update": "1970-01-01T00:00:00",
      "savings_hbd_last_interest_payment": "1970-01-01T00:00:00",
      "savings_withdraw_requests": 0,
      "reward_hbd_balance": "0.000 HBD",
      "reward_hive_balance": "0.000 HIVE",
      "reward_vesting_balance": "0.000000 VESTS",
      "reward_vesting_hive": "0.000 HIVE",
      "vesting_shares": "598442.432741 VESTS",
      "delegated_vesting_shares": "0.000000 VESTS",
      "received_vesting_shares": "0.000000 VESTS",
      "vesting_withdraw_rate": "0.000000 VESTS",
      "post_voting_power": "598442.432741 VESTS",
      "next_vesting_withdrawal": "1969-12-31T23:59:59",
      "withdrawn": 0,
      "to_withdraw": 0,
      "withdraw_routes": 0,
      "pending_transfers": 0,
      "curation_rewards": 0,
      "posting_rewards": 604589,
      "proxied_vsf_votes": [0, 0, 0, 0],
      "witnesses_voted_for": 0,
      "last_post": "2021-03-23T18:05:48",
      "last_root_post": "2021-03-23T18:05:48",
      "last_vote_time": "1970-01-01T00:00:00",
      "post_bandwidth": 0,
      "pending_claimed_accounts": 0,
      "delayed_votes": [
        {
          "time": "2021-02-24T05:08:21",
          "val": "11550765516955"
        },
        {
          "time": "2021-02-26T15:46:06",
          "val": "633465684569"
        },
        {
          "time": "2021-03-07T17:54:39",
          "val": "1000000037683"
        },
        {
          "time": "2021-03-16T05:54:33",
          "val": "999978763511"
        },
        {
          "time": "2021-03-18T06:06:00",
          "val": "1000000171317"
        }
      ],
      "vesting_balance": "0.000 HIVE",
      "reputation": "88826789432105",
      "transfer_history": [],
      "market_history": [],
      "post_history": [],
      "vote_history": [],
      "other_history": [],
      "witness_votes": [],
      "tags_usage": [],
      "guest_bloggers": []
    }
    

##### Example `curl`[](#condenser_api.get_accounts-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_accounts", "params":[["hiveio"]], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_accounts", "params":[["hiveio", "alice"], true], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_active_votes)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-active-votes)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-active-votes)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20active%20votes)**

#### condenser\_api.get\_active\_votes[](#condenser_api.get_active_votes)

Returns all votes for the given post. Parameters: `author:string`; `permlink:string`

`author` (string)

`permlink` (string)

 

`"hiveio"`

`"firstpost"`

Queries votes for content with a slug `@hiveio/firstpost`

`"alice"`

`"a-post-by-alice"`

Queries votes for content with a slug `@alice/a-post-by-alice`

##### Query Parameters JSON[](#condenser_api.get_active_votes-parameter_json)

    ["", ""]
    

##### Expected Response JSON[](#condenser_api.get_active_votes-expected_response_json)

    [
      {
        "voter": "",
        "weight": "",
        "rshares": 0,
        "percent": 0,
        "reputation": "",
        "time": "1970-01-01T00:00:00"
      }
    ]
    

##### Example `curl`[](#condenser_api.get_active_votes-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_active_votes", "params":["hiveio", "firstpost"], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_active_votes", "params":["alice", "a-post-by-alice"], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_active_witnesses)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-active-witnesses)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-active-witnesses)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/witnesses)
    
*   **[Related](/search/?q=get%20active%20witnesses)**

#### condenser\_api.get\_active\_witnesses[](#condenser_api.get_active_witnesses)

Returns the list of active witnesses.

Also see: [database\_api.get\_active\_witnesses](/apidefinitions/#database_api.get_active_witnesses)

##### Query Parameters JSON[](#condenser_api.get_active_witnesses-parameter_json)

    []
    

##### Expected Response JSON[](#condenser_api.get_active_witnesses-expected_response_json)

    []
    

##### Example `curl`[](#condenser_api.get_active_witnesses-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_active_witnesses", "params":[], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_block)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-block)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-block)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20block)**

#### condenser\_api.get\_block[](#condenser_api.get_block)

Returns a block. Parameters: `block_num:int`

`block_num` (int)

 

`1`

Queries the very first block.

`8675309`

Queries block number 8,675,309.

`62396745`

Queries block number 62,396,745.

Also see: [block\_api.get\_block](/apidefinitions/#block_api.get_block)

##### Query Parameters JSON[](#condenser_api.get_block-parameter_json)

    [1]
    

##### Expected Response JSON[](#condenser_api.get_block-expected_response_json)

    {
      "previous": "0000000000000000000000000000000000000000",
      "timestamp": "2016-03-24T16:05:00",
      "witness": "initminer",
      "transaction_merkle_root": "0000000000000000000000000000000000000000",
      "extensions": [],
      "witness_signature": "204f8ad56a8f5cf722a02b035a61b500aa59b9519b2c33c77a80c0a714680a5a5a7a340d909d19996613c5e4ae92146b9add8a7a663eef37d837ef881477313043",
      "transactions": [],
      "block_id": "0000000109833ce528d5bbfb3f6225b39ee10086",
      "signing_key": "STM8GC13uCZbP44HzMLV6zPZGwVQ8Nt4Kji8PapsPiNq1BK153XTX",
      "transaction_ids": []
    }
    

##### Example `curl`[](#condenser_api.get_block-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_block", "params":[1], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_block", "params":[8675309], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_block", "params":[62396745], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_block_header)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-block-header)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-block-header)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20block%20header)**

#### condenser\_api.get\_block\_header[](#condenser_api.get_block_header)

Returns a block header. Parameters: `block_num:int`

`block_num` (int)

 

`1`

Queries the block headers for the very first block.

`8675309`

Queries block headers for block number 8,675,309.

`62396745`

Queries block headers for block number 62,396,745.

Also see: [block\_api.get\_block\_header](/apidefinitions/#block_api.get_block_header)

##### Query Parameters JSON[](#condenser_api.get_block_header-parameter_json)

    [1]
    

##### Expected Response JSON[](#condenser_api.get_block_header-expected_response_json)

    {
      "previous": "0000000000000000000000000000000000000000",
      "timestamp": "2016-03-24T16:05:00",
      "witness": "initminer",
      "transaction_merkle_root": "0000000000000000000000000000000000000000",
      "extensions": []
    }
    

##### Example `curl`[](#condenser_api.get_block_header-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_block_header", "params":[1], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_block_header", "params":[8675309], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_block_header", "params":[62396745], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_blog)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-blog)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-blog)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20blog)**

#### condenser\_api.get\_blog[](#condenser_api.get_blog)

Returns the list of blog entries for an account. Parameters: `account:string`; `start_entry_id:int`; `limit:int` up to 500

`account` (string)

`start_entry_id` (int)

`limit` (int)

 

“hiveio”

`0`

`1`

Queries the blog for the account named “hiveio”, up to one result.

“alice”

`0`

`50`

Queries the blog for the account named “alice”, up to 50 results.

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#condenser_apiget_blog)

##### Query Parameters JSON[](#condenser_api.get_blog-parameter_json)

    ["hiveio", 0, 1]
    

##### Expected Response JSON[](#condenser_api.get_blog-expected_response_json)

    [
      {
        "comment": {
          "id": 0,
          "author": "hiveio",
          "permlink": "firstpost",
          "category": "meta",
          "parent_author": "",
          "parent_permlink": "meta",
          "title": "Welcome to Hive!",
          "body": "Hive is a social media platform where anyone can earn HIVE points by posting. The more people who like a post, the more HIVE the poster earns. Anyone can sell their HIVE for cash or vest it to boost their voting power.",
          "json_metadata": "",
          "last_update": "2016-03-30T18:30:18",
          "created": "2016-03-30T18:30:18",
          "active": "2018-04-09T12:00:42",
          "last_payout": "2016-08-24T19:59:42",
          "depth": 0,
          "children": 336,
          "net_rshares": 0,
          "abs_rshares": 0,
          "vote_rshares": 0,
          "children_abs_rshares": "26169324897669",
          "cashout_time": "1969-12-31T23:59:59",
          "max_cashout_time": "1969-12-31T23:59:59",
          "total_vote_weight": 0,
          "reward_weight": 10000,
          "total_payout_value": {
            "amount": "942",
            "precision": 3,
            "nai": "@@000000013"
          },
          "curator_payout_value": {
            "amount": "756",
            "precision": 3,
            "nai": "@@000000013"
          },
          "author_rewards": 3548,
          "net_votes": 90,
          "root_author": "hiveio",
          "root_permlink": "firstpost",
          "max_accepted_payout": {
            "amount": "1000000000",
            "pecision": 3,
            "nai": "@@000000013"
          },
          "percent_hbd": 10000,
          "allow_replies": true,
          "allow_votes": true,
          "allow_curation_rewards": true,
          "beneficiaries": []
        },
        "blog": "hiveio",
        "reblog_on": "1970-01-01T00:00:00",
        "entry_id": 0
      }
    ]
    

##### Example `curl`[](#condenser_api.get_blog-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_blog", "params":["hiveio",0,1], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_blog", "params":["alice",0,50], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-blog-authors)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-blog-authors)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20blog%20authors)**

#### condenser\_api.get\_blog\_authors[](#condenser_api.get_blog_authors)

Returns a list of authors that have had their content reblogged on a given blog account. Parameters: `account:string`

`account` (string)

 

`"hiveio"`

Queries for account named “hiveio”.

`"alice"`

Queries for accounts named alice”.

##### Query Parameters JSON[](#condenser_api.get_blog_authors-parameter_json)

    [""]
    

##### Expected Response JSON[](#condenser_api.get_blog_authors-expected_response_json)

    [{"author": "", "count": 0}]
    

##### Example `curl`[](#condenser_api.get_blog_authors-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_blog_authors", "params":["hiveio"], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_blog_authors", "params":["alice"], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_blog_entries)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-blog-entries)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-blog-entries)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20blog%20entries)**

#### condenser\_api.get\_blog\_entries[](#condenser_api.get_blog_entries)

Returns a list of blog entries for an account. Parameters: `account:string`; `start_entry_id:int`; `limit:int` up to 500

`account` (string)

`start_entry_id` (int)

`limit` (int)

 

“hiveio”

`0`

`1`

Queries the blog entries for the account named “hiveio”, up to one result.

“alice”

`0`

`50`

Queries the blog entries for the account named “alice”, up to 50 results.

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#condenser_apiget_blog_entries)

##### Query Parameters JSON[](#condenser_api.get_blog_entries-parameter_json)

    ["hiveio", 0, 1]
    

##### Expected Response JSON[](#condenser_api.get_blog_entries-expected_response_json)

    [
      {
        "author": "hiveio",
        "permlink": "firstpost",
        "blog": "hiveio",
        "reblog_on": "1970-01-01T00:00:00",
        "entry_id": 0
      }
    ]
    

##### Example `curl`[](#condenser_api.get_blog_entries-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_blog_entries", "params":["hiveio",0,1], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_blog_entries", "params":["alice",0,50], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_chain_properties)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-chain-properties)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-chain-properties)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20chain%20properties)**

#### condenser\_api.get\_chain\_properties[](#condenser_api.get_chain_properties)

Returns the chain properties.

##### Query Parameters JSON[](#condenser_api.get_chain_properties-parameter_json)

    []
    

##### Expected Response JSON[](#condenser_api.get_chain_properties-expected_response_json)

    {
      "account_creation_fee": "0.100 HIVE",
      "maximum_block_size": 131072,
      "hbd_interest_rate": 1000,
      "account_subsidy_limit": 0
    }
    

##### Example `curl`[](#condenser_api.get_chain_properties-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_chain_properties", "params":[], "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF17**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_comment_discussions_by_payout)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-comment-discussions-by-payout)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-comment-discussions-by-payout)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/tags)
    
*   **[Related](/search/?q=get%20comment%20discussions%20payout)**

#### condenser\_api.get\_comment\_discussions\_by\_payout[](#condenser_api.get_comment_discussions_by_payout)

Returns a list of discussions based on payout.

Also see: [tags\_api.get\_comment\_discussions\_by\_payout](/apidefinitions/#tags_api.get_comment_discussions_by_payout)

##### Query Parameters JSON[](#condenser_api.get_comment_discussions_by_payout-parameter_json)

    [
      {
        "tag": "",
        "limit": 0,
        "filter_tags": [],
        "select_authors": [],
        "select_tags": [],
        "truncate_body": 0
      }
    ]
    

##### Expected Response JSON[](#condenser_api.get_comment_discussions_by_payout-expected_response_json)

    []
    

##### Example `curl`[](#condenser_api.get_comment_discussions_by_payout-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_comment_discussions_by_payout", "params":[{"tag":"hive","limit":1}], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_comment_discussions_by_payout", "params":[{"tag":"photography","limit":10,"truncate_body":0}], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_config)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-config)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-config)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20config)**

#### condenser\_api.get\_config[](#condenser_api.get_config)

Returns information about compile-time constants. See: [Understanding Configuration Values](/tutorials-recipes/understanding-configuration-values.html)

Also see: [database\_api.get\_config](/apidefinitions/#database_api.get_config)

##### Query Parameters JSON[](#condenser_api.get_config-parameter_json)

    []
    

##### Expected Response JSON[](#condenser_api.get_config-expected_response_json)

    {}
    

##### Example `curl`[](#condenser_api.get_config-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_config", "params":[], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_content)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-content)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-content)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/comments)
    
*   **[Related](/search/?q=get%20content)**

#### condenser\_api.get\_content[](#condenser_api.get_content)

Returns the content (post or comment). Parameters: `author:string`; `permlink:string`

`author` (string)

`permlink` (string)

 

`"hiveio"`

`"firstpost"`

Queries content with a slug `@hiveio/firstpost`

`"alice"`

`"a-post-by-alice"`

Queries content with a slug `@alice/a-post-by-alice`

##### Query Parameters JSON[](#condenser_api.get_content-parameter_json)

    ["", ""]
    

##### Expected Response JSON[](#condenser_api.get_content-expected_response_json)

    {
      "id": 0,
      "author": "",
      "permlink": "",
      "category": "",
      "parent_author": "",
      "parent_permlink": "",
      "title": "",
      "body": "",
      "json_metadata": "",
      "last_update": "1970-01-01T00:00:00",
      "created": "1970-01-01T00:00:00",
      "active": "1970-01-01T00:00:00",
      "last_payout": "1970-01-01T00:00:00",
      "depth": 0,
      "children": 0,
      "net_rshares": 0,
      "abs_rshares": 0,
      "vote_rshares": 0,
      "children_abs_rshares": 0,
      "cashout_time": "1970-01-01T00:00:00",
      "max_cashout_time": "1970-01-01T00:00:00",
      "total_vote_weight": 0,
      "reward_weight": 0,
      "total_payout_value": "0.000 HIVE",
      "curator_payout_value": "0.000 HIVE",
      "author_rewards": 0,
      "net_votes": 0,
      "root_author": "",
      "root_permlink": "",
      "max_accepted_payout": "0.000 HIVE",
      "percent_hbd": 0,
      "allow_replies": false,
      "allow_votes": false,
      "allow_curation_rewards": false,
      "beneficiaries": [],
      "url": "",
      "root_title": "",
      "pending_payout_value": "0.000 HIVE",
      "total_pending_payout_value": "0.000 HIVE",
      "active_votes": [],
      "replies": [],
      "author_reputation": 0,
      "promoted": "0.000 HIVE",
      "body_length": 0,
      "reblogged_by": []
    }
    

##### Example `curl`[](#condenser_api.get_content-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_content", "params":["hiveio", "firstpost"], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_content", "params":["alice", "a-post-by-alice"], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_content_replies)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-content-replies)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-content-replies)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20content%20replies)**

#### condenser\_api.get\_content\_replies[](#condenser_api.get_content_replies)

Returns a list of replies. Parameters: `author:string`; `permlink:string`

`author` (string)

`permlink` (string)

 

`"hiveio"`

`"firstpost"`

Queries replies for a slug `@hiveio/firstpost`

`"alice"`

`"a-post-by-alice"`

Queries replies for a slug `@alice/a-post-by-alice`

Also see: [tags\_api.get\_content\_replies](/apidefinitions/#tags_api.get_content_replies)

##### Query Parameters JSON[](#condenser_api.get_content_replies-parameter_json)

    ["", ""]
    

##### Expected Response JSON[](#condenser_api.get_content_replies-expected_response_json)

    {
      "id": 0,
      "author": "",
      "permlink": "",
      "category": "",
      "parent_author": "",
      "parent_permlink": "",
      "title": "",
      "body": "",
      "json_metadata": "",
      "last_update": "1970-01-01T00:00:00",
      "created": "1970-01-01T00:00:00",
      "active": "1970-01-01T00:00:00",
      "last_payout": "1970-01-01T00:00:00",
      "depth": 0,
      "children": 0,
      "net_rshares": 0,
      "abs_rshares": 0,
      "vote_rshares": 0,
      "children_abs_rshares": 0,
      "cashout_time": "1970-01-01T00:00:00",
      "max_cashout_time": "1970-01-01T00:00:00",
      "total_vote_weight": 0,
      "reward_weight": 0,
      "total_payout_value": "0.000 HIVE",
      "curator_payout_value": "0.000 HIVE",
      "author_rewards": 0,
      "net_votes": 0,
      "root_author": "",
      "root_permlink": "",
      "max_accepted_payout": "0.000 HIVE",
      "percent_hbd": 0,
      "allow_replies": false,
      "allow_votes": false,
      "allow_curation_rewards": false,
      "beneficiaries": [],
      "url": "",
      "root_title": "",
      "pending_payout_value": "0.000 HIVE",
      "total_pending_payout_value": "0.000 HIVE",
      "active_votes": [],
      "replies": [],
      "author_reputation": 0,
      "promoted": "0.000 HIVE",
      "body_length": 0,
      "reblogged_by": []
    }
    

##### Example `curl`[](#condenser_api.get_content_replies-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_content_replies", "params":["hiveio", "firstpost"], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_content_replies", "params":["alice", "a-post-by-alice"], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_conversion_requests)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-conversion-requests)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-conversion-requests)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20conversion%20requests)**

#### condenser\_api.get\_conversion\_requests[](#condenser_api.get_conversion_requests)

Returns a list of conversion request. Parameters: `id:integer`

`id` (int)

 

`1234`

Queries a conversion request with the id of 1234.

Also see: [database\_api.list\_hbd\_conversion\_requests](/apidefinitions/#database_api.list_hbd_conversion_requests)

##### Query Parameters JSON[](#condenser_api.get_conversion_requests-parameter_json)

    [0]
    

##### Expected Response JSON[](#condenser_api.get_conversion_requests-expected_response_json)

    []
    

##### Example `curl`[](#condenser_api.get_conversion_requests-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_conversion_requests", "params":[1234], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_current_median_history_price)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-current-median-history-price)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-current-median-history-price)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20current%20median%20history%20price)**

#### condenser\_api.get\_current\_median\_history\_price[](#condenser_api.get_current_median_history_price)

##### Query Parameters JSON[](#condenser_api.get_current_median_history_price-parameter_json)

    []
    

##### Expected Response JSON[](#condenser_api.get_current_median_history_price-expected_response_json)

    {"base": "0.000 HIVE", "quote": "0.000 HIVE"}
    

##### Example `curl`[](#condenser_api.get_current_median_history_price-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_current_median_history_price", "params":[], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_discussions_by_author_before_date)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-discussions-by-author-before-date)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-discussions-by-author-before-date)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/tags)
    
*   **[Related](/search/?q=get%20discussions%20author%20date)**

#### condenser\_api.get\_discussions\_by\_author\_before\_date[](#condenser_api.get_discussions_by_author_before_date)

Returns a list of discussions based on author before date.

Also see: [tags\_api.get\_discussions\_by\_author\_before\_date](/apidefinitions/#tags_api.get_discussions_by_author_before_date), [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#condenser_apiget_discussions_by_author_before_date)

##### Query Parameters JSON[](#condenser_api.get_discussions_by_author_before_date-parameter_json)

    ["", "", "1970-01-01T00:00:00", 100]
    

##### Expected Response JSON[](#condenser_api.get_discussions_by_author_before_date-expected_response_json)

    []
    

##### Example `curl`[](#condenser_api.get_discussions_by_author_before_date-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_discussions_by_author_before_date", "params":["hiveio","firstpost","2016-04-19T22:49:43",1], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_dynamic_global_properties)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-dynamic-global-properties)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-dynamic-global-properties)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/dynamicglobalproperties)
    
*   **[Related](/search/?q=get%20dynamic%20global%20properties)**

#### condenser\_api.get\_dynamic\_global\_properties[](#condenser_api.get_dynamic_global_properties)

Returns the current dynamic global properties. See: [Understanding Dynamic Global Properties](/tutorials-recipes/understanding-dynamic-global-properties.html)

Also see: [database\_api.get\_dynamic\_global\_properties](/apidefinitions/#database_api.get_dynamic_global_properties)

##### Query Parameters JSON[](#condenser_api.get_dynamic_global_properties-parameter_json)

    []
    

##### Expected Response JSON[](#condenser_api.get_dynamic_global_properties-expected_response_json)

    {
      "head_block_number": 0,
      "head_block_id": "0000000000000000000000000000000000000000",
      "time": "1970-01-01T00:00:00",
      "current_witness": "",
      "total_pow": "18446744073709551615",
      "num_pow_witnesses": 0,
      "virtual_supply": "0.000 HIVE",
      "current_supply": "0.000 HIVE",
      "confidential_supply": "0.000 HIVE",
      "current_hbd_supply": "0.000 HIVE",
      "confidential_hbd_supply": "0.000 HIVE",
      "total_vesting_fund_hive": "0.000 HIVE",
      "total_vesting_shares": "0.000 HIVE",
      "total_reward_fund_hive": "0.000 HIVE",
      "total_reward_shares2": "0",
      "pending_rewarded_vesting_shares": "0.000 HIVE",
      "pending_rewarded_vesting_hive": "0.000 HIVE",
      "hbd_interest_rate": 0,
      "hbd_print_rate": 10000,
      "maximum_block_size": 0,
      "current_aslot": 0,
      "recent_slots_filled": "0",
      "participation_count": 0,
      "last_irreversible_block_num": 0,
      "vote_power_reserve_rate": 40
    }
    

##### Example `curl`[](#condenser_api.get_dynamic_global_properties-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_dynamic_global_properties", "params":[], "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF14**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_escrow)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-escrow)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-escrow)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20escrow)**

#### condenser\_api.get\_escrow[](#condenser_api.get_escrow)

Returns the escrow for a certain account by id.

Also see: [database\_api.list\_escrows](/apidefinitions/#database_api.list_escrows)

##### Query Parameters JSON[](#condenser_api.get_escrow-parameter_json)

    ["", 0]
    

##### Expected Response JSON[](#condenser_api.get_escrow-expected_response_json)

    null
    

##### Example `curl`[](#condenser_api.get_escrow-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_escrow", "params":["hiveio", 1234], "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF17**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_expiring_vesting_delegations)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#api-call)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-expiring-vesting-delegations)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/delegations)
    
*   **[Related](/search/?q=get%20expiring%20vesting%20delegations)**

#### condenser\_api.get\_expiring\_vesting\_delegations[](#condenser_api.get_expiring_vesting_delegations)

Returns the expiring vesting delegations for an account. Parameters: `account:string`, `after:timestamp`

`account` (string)

`after` (timestamp)

 

`"hiveio"`

`"2018-01-01T00:00:00"`

Queries for expiring vesting after January 1st, 2018.

`"alice"`

`"2017-12-01T00:00:00"`

Queries for expiring vesting after December 1st, 2017.

##### Query Parameters JSON[](#condenser_api.get_expiring_vesting_delegations-parameter_json)

    ["", "1970-01-01T00:00:00"]
    

##### Expected Response JSON[](#condenser_api.get_expiring_vesting_delegations-expected_response_json)

    [
      {
        "id": 0,
        "delegator": "",
        "vesting_shares": "0.000000 VESTS",
        "expiration": "1970-01-01T00:00:00"
      }
    ]
    

##### Example `curl`[](#condenser_api.get_expiring_vesting_delegations-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_expiring_vesting_delegations", "params":["hiveio","2018-01-01T00:00:00"], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_expiring_vesting_delegations", "params":["alice","2017-12-01T00:00:00"], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_feed_history)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-feed-history)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-feed-history)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20feed%20history)**

#### condenser\_api.get\_feed\_history[](#condenser_api.get_feed_history)

Returns the history of price feed values.

Also see: [database\_api.get\_feed\_history](/apidefinitions/#database_api.get_feed_history)

##### Query Parameters JSON[](#condenser_api.get_feed_history-parameter_json)

    []
    

##### Expected Response JSON[](#condenser_api.get_feed_history-expected_response_json)

    {
      "id": 0,
      "current_median_history": {"base": "0.000 HIVE", "quote": "0.000 HIVE"},
      "price_history": []
    }
    

##### Example `curl`[](#condenser_api.get_feed_history-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_feed_history", "params":[], "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF9**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_follow_count)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-follow-count)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-follow-count)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/followers)
    
*   **[Related](/search/?q=get%20follow%20count)**

#### condenser\_api.get\_follow\_count[](#condenser_api.get_follow_count)

Returns the count of followers/following for an account. Parameters: `account:string`

`account` (string)

 

`"hiveio"`

Queries the account named `hiveio`.

`"alice"`

Queries the account named `alice`.

##### Query Parameters JSON[](#condenser_api.get_follow_count-parameter_json)

    [""]
    

##### Expected Response JSON[](#condenser_api.get_follow_count-expected_response_json)

    {
      "account": "",
      "follower_count": 0,
      "following_count": 0
    }
    

##### Example `curl`[](#condenser_api.get_follow_count-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_follow_count", "params":["hiveio"], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_follow_count", "params":["alice"], "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF9**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_followers)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-followers)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-followers)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/followers)
    
*   **[Related](/search/?q=get%20followers)**

#### condenser\_api.get\_followers[](#condenser_api.get_followers)

Returns the list of followers for an account. Parameters: `account:string`; `start:string` (account to start from); `type:string` e.g.: `blog`; `limit:int` up to 1000

`account` (string)

`start` (string)

`type` (string)

`limit` (int)

 

`"hiveio"`

`null`

`"blog"`

`10`

Queries for follows of the account named `hiveio`, up to 10 results.

`"alice"`

`null`

`"ignore"`

`100`

Queries for mutes of the account named `alice`, up to 100 results.

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#condenser_apiget_followers)

##### Query Parameters JSON[](#condenser_api.get_followers-parameter_json)

    ["", "", "", 1]
    

##### Expected Response JSON[](#condenser_api.get_followers-expected_response_json)

    []
    

##### Example `curl`[](#condenser_api.get_followers-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_followers", "params":["hiveio",null,"blog",10], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_followers", "params":["alice",null,"ignore",100], "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF9**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_following)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-following)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-following)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/followers)
    
*   **[Related](/search/?q=get%20following)**

#### condenser\_api.get\_following[](#condenser_api.get_following)

Returns the list of accounts that are following an account. Parameters: `account:string`; `start:string` (account to start from); `type:string` e.g.: `blog`; `limit:int` up to 1000

`account` (string)

`start` (string)

`type` (string)

`limit` (int)

 

`"hiveio"`

`null`

`"blog"`

`10`

Queries for follows of the account named `hiveio`, up to 10 results.

`"alice"`

`null`

`"ignore"`

`100`

Queries for mutes of the account named `alice`, up to 100 results.

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#condenser_apiget_following)

##### Query Parameters JSON[](#condenser_api.get_following-parameter_json)

    ["", "", "", 1]
    

##### Expected Response JSON[](#condenser_api.get_following-expected_response_json)

    []
    

##### Example `curl`[](#condenser_api.get_following-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_following", "params":["hiveio",null,"blog",10], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_following", "params":["alice",null,"ignore",100], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_hardfork_version)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-hardfork-version)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-hardfork-version)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20hardfork%20version)**

#### condenser\_api.get\_hardfork\_version[](#condenser_api.get_hardfork_version)

Returns the current hardfork version.

Also see: [database\_api.get\_hardfork\_properties](/apidefinitions/#database_api.get_hardfork_properties)

##### Query Parameters JSON[](#condenser_api.get_hardfork_version-parameter_json)

    []
    

##### Expected Response JSON[](#condenser_api.get_hardfork_version-expected_response_json)

    "0.0.0"
    

##### Example `curl`[](#condenser_api.get_hardfork_version-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_hardfork_version", "params":[], "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF16**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_key_references)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-key-references)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-key-references)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20key%20references)**

#### condenser\_api.get\_key\_references[](#condenser_api.get_key_references)

Returns all accounts that have the key associated with their owner or active authorities.

Also see: [account\_by\_key\_api.get\_key\_references](/apidefinitions/#account_by_key_api.get_key_references)

##### Query Parameters JSON[](#condenser_api.get_key_references-parameter_json)

    [
      [
        "STM6vJmrwaX5TjgTS9dPH8KsArso5m91fVodJvv91j7G765wqcNM9"
      ]
    ]
    

##### Expected Response JSON[](#condenser_api.get_key_references-expected_response_json)

    [["hiveio"]]
    

##### Example `curl`[](#condenser_api.get_key_references-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_key_references", "params":[["STM6vJmrwaX5TjgTS9dPH8KsArso5m91fVodJvv91j7G765wqcNM9"]], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_market_history)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#api-call)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-market-history)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20market%20history)**

#### condenser\_api.get\_market\_history[](#condenser_api.get_market_history)

Returns the market history for the internal HBD:HIVE market. Parameters: `bucket_seconds:int`; `start:timestamp`; `end:timestamp`

`bucket_seconds` (int)

`start` (timestamp)

`end` (timestamp)

 

`15`

`"2018-01-01T00:00:00"`

`"2018-01-02T00:00:00"`

Queries for market history between January 1st, 2018 and January 2nd, 2018, segmented by 15 seconds.

`60`

`"2018-01-01T00:00:00"`

`"2018-01-02T00:00:00"`

Queries for market history between January 1st, 2018 and January 2nd, 2018, segmented by one minute.

`300`

`"2018-01-01T00:00:00"`

`"2018-01-02T00:00:00"`

Queries for market history between January 1st, 2018 and January 2nd, 2018, segmented by five minutes.

`3600`

`"2018-01-01T00:00:00"`

`"2018-01-02T00:00:00"`

Queries for market history between January 1st, 2018 and January 2nd, 2018, segmented by one hour.

`86400`

`"2018-01-01T00:00:00"`

`"2018-01-02T00:00:00"`

Queries for market history between January 1st, 2018 and January 2nd, 2018, segmented by one day.

Also see: [market\_history\_api.get\_market\_history](/apidefinitions/#market_history_api.get_market_history)

##### Query Parameters JSON[](#condenser_api.get_market_history-parameter_json)

    [0, "1970-01-01T00:00:00", "1970-01-01T00:00:00"]
    

##### Expected Response JSON[](#condenser_api.get_market_history-expected_response_json)

    [
      {
        "id": 0,
        "open": "1970-01-01T00:00:00",
        "seconds": 0,
        "hive": {
          "high": 0,
          "low": 0,
          "open": 0,
          "close": 0,
          "volume": 0
        },
        "non_hive": {
          "high": 0,
          "low": 0,
          "open": 0,
          "close": 0,
          "volume": 0
        }
      }
    ]
    

##### Example `curl`[](#condenser_api.get_market_history-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_market_history", "params":[15,"2018-01-01T00:00:00","2018-01-02T00:00:00"], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_market_history", "params":[60,"2018-01-01T00:00:00","2018-01-02T00:00:00"], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_market_history", "params":[300,"2018-01-01T00:00:00","2018-01-02T00:00:00"], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_market_history", "params":[3600,"2018-01-01T00:00:00","2018-01-02T00:00:00"], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_market_history", "params":[86400,"2018-01-01T00:00:00","2018-01-02T00:00:00"], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_market_history_buckets)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-market-history-buckets)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-market-history-buckets)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20market%20history%20buckets)**

#### condenser\_api.get\_market\_history\_buckets[](#condenser_api.get_market_history_buckets)

Returns the bucket seconds being tracked by the plugin.

Also see: [market\_history\_api.get\_market\_history\_buckets](/apidefinitions/#market_history_api.get_market_history_buckets)

##### Query Parameters JSON[](#condenser_api.get_market_history_buckets-parameter_json)

    []
    

##### Expected Response JSON[](#condenser_api.get_market_history_buckets-expected_response_json)

    [15, 60, 300, 3600, 86400]
    

##### Example `curl`[](#condenser_api.get_market_history_buckets-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_market_history_buckets", "params":[], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_next_scheduled_hardfork)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-next-scheduled-hardfork)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-next-scheduled-hardfork)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20next%20scheduled%20hardfork)**

#### condenser\_api.get\_next\_scheduled\_hardfork[](#condenser_api.get_next_scheduled_hardfork)

Returns the next scheduled hardfork.

Also see: [database\_api.get\_hardfork\_properties](/apidefinitions/#database_api.get_hardfork_properties), [hardfork](/apidefinitions/#broadcast_ops_hardfork)

##### Query Parameters JSON[](#condenser_api.get_next_scheduled_hardfork-parameter_json)

    []
    

##### Expected Response JSON[](#condenser_api.get_next_scheduled_hardfork-expected_response_json)

    {
      "hf_version": "0.0.0",
      "live_time": "1970-01-01T00:00:00"
    }
    

##### Example `curl`[](#condenser_api.get_next_scheduled_hardfork-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_next_scheduled_hardfork", "params":[], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_open_orders)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-open-orders)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-open-orders)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20open%20orders)**

#### condenser\_api.get\_open\_orders[](#condenser_api.get_open_orders)

Returns the open orders for an account. `account:string`

Also see: [database\_api.list\_limit\_orders](/apidefinitions/#database_api.list_limit_orders)

##### Query Parameters JSON[](#condenser_api.get_open_orders-parameter_json)

    [""]
    

##### Expected Response JSON[](#condenser_api.get_open_orders-expected_response_json)

    []
    

##### Example `curl`[](#condenser_api.get_open_orders-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_open_orders", "params":["hiveio"], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_open_orders", "params":["alice"], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_ops_in_block)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-ops-in-block)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-ops-in-block)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20ops%20block)**

#### condenser\_api.get\_ops\_in\_block[](#condenser_api.get_ops_in_block)

Returns all operations contained in a block. Parameters: `block_num:int`; `only_virtual:boolean`

`block_num` (int)

`only_virtual` (boolean)

 

`1`

`false`

Queries the operations in block #1.

`5443322`

`true`

Queries only the virtual operations in block #5,443,322.

Also see: [account\_history\_api.get\_ops\_in\_block](/apidefinitions/#account_history_api.get_ops_in_block)

##### Query Parameters JSON[](#condenser_api.get_ops_in_block-parameter_json)

    [0, false]
    

##### Expected Response JSON[](#condenser_api.get_ops_in_block-expected_response_json)

    [
      {
        "trx_id": "0000000000000000000000000000000000000000",
        "block": 0,
        "trx_in_block": 0,
        "op_in_trx": 0,
        "virtual_op": 0,
        "timestamp": "2016-10-01T06:31:24",
        "op": [
          "producer_reward",
          {
            "producer": "",
            "vesting_shares": "0.000000 VESTS"
          }
        ]
      }
    ]
    

##### Example `curl`[](#condenser_api.get_ops_in_block-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_ops_in_block", "params":[1,false], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_ops_in_block", "params":[5443322,true], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_order_book)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-order-book)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-order-book)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20order%20book)**

#### condenser\_api.get\_order\_book[](#condenser_api.get_order_book)

Returns the internal market order book. Parameters: `limit:int` up to 500

`limit` (int)

 

`10`

Queries up to 10 items in the order book.

`500`

Queries up to 500 items in the order book.

Also see: [database\_api.get\_order\_book](/apidefinitions/#database_api.get_order_book), [market\_history\_api.get\_order\_book](/apidefinitions/#market_history_api.get_order_book)

##### Query Parameters JSON[](#condenser_api.get_order_book-parameter_json)

    [0]
    

##### Expected Response JSON[](#condenser_api.get_order_book-expected_response_json)

    {"bids": [], "asks": []}
    

##### Example `curl`[](#condenser_api.get_order_book-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_order_book", "params":[10], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_order_book", "params":[50], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_owner_history)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-owner-history)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-owner-history)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20owner%20history)**

#### condenser\_api.get\_owner\_history[](#condenser_api.get_owner_history)

Returns the owner history of an account. Parameters: `account:string`

`account` (string)

 

`"hiveio"`

Queries the owner history for account named “hiveio”.

Also see: [database\_api.list\_owner\_histories](/apidefinitions/#database_api.list_owner_histories)

##### Query Parameters JSON[](#condenser_api.get_owner_history-parameter_json)

    [""]
    

##### Expected Response JSON[](#condenser_api.get_owner_history-expected_response_json)

    []
    

##### Example `curl`[](#condenser_api.get_owner_history-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_owner_history", "params":["hiveio"], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-potential-signatures)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-potential-signatures)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20potential%20signatures)**

#### condenser\_api.get\_potential\_signatures[](#condenser_api.get_potential_signatures)

This method will return the set of all public keys that could possibly sign for a given transaction.

Also see: [database\_api.get\_potential\_signatures](/apidefinitions/#database_api.get_potential_signatures)

##### Query Parameters JSON[](#condenser_api.get_potential_signatures-parameter_json)

    [
      {
        "ref_block_num": 0,
        "ref_block_prefix": 0,
        "expiration": "1970-01-01T00:00:00",
        "operations": [],
        "extensions": [],
        "signatures": []
      }
    ]
    

##### Expected Response JSON[](#condenser_api.get_potential_signatures-expected_response_json)

    []
    

##### Example `curl`[](#condenser_api.get_potential_signatures-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_potential_signatures", "params":[{"ref_block_num":1097,"ref_block_prefix":2181793527,"expiration":"2016-03-24T18:00:21","operations":[["pow",{"worker_account":"cloop3","block_id":"00000449f7860b82b4fbe2f317c670e9f01d6d9a","nonce":3899,"work":{"worker":"STM7P5TDnA87Pj9T4mf6YHrhzjC1KbPZpNxLWCcVcHxNYXakpoT4F","input":"ae8e7c677119d22385f8c48026fee7aad7bba693bf788d7f27047f40b47738c0","signature":"1f38fe9a3f9989f84bd94aa5bbc88beaf09b67f825aa4450cf5105d111149ba6db560b582c7dbb026c7fc9c2eb5051815a72b17f6896ed59d3851d9a0f9883ca7a","work":"000e7b209d58f2e64b36e9bf12b999c6c7af168cc3fc41eb7f8a4bf796c174c3"},"props":{"account_creation_fee":{"amount":"100000","precision":3,"nai":"@@000000021"},"maximum_block_size":131072,"hbd_interest_rate":1000}}]],"extensions":[],"signatures":[]}], "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF14**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_reblogged_by)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-reblogged-by)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-reblogged-by)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/reblogs)
    
*   **[Related](/search/?q=get%20reblogged)**

#### condenser\_api.get\_reblogged\_by[](#condenser_api.get_reblogged_by)

Returns a list of authors that have reblogged a post. Parameters: `author:string`; `permlink:string`

`author` (string)

`permlink` (string)

 

`"hiveio"`

`"firstpost"`

Queries reblogs for content with a slug `@hiveio/firstpost`

`"alice"`

`"a-post-by-alice"`

Queries reblogs for content with a slug `@alice/a-post-by-alice`

##### Query Parameters JSON[](#condenser_api.get_reblogged_by-parameter_json)

    ["", ""]
    

##### Expected Response JSON[](#condenser_api.get_reblogged_by-expected_response_json)

    []
    

##### Example `curl`[](#condenser_api.get_reblogged_by-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_reblogged_by", "params":["hiveio","firstpost"], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_reblogged_by", "params":["alice","a-post-by-alice"], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_recent_trades)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-recent-trades)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-recent-trades)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20recent%20trades)**

#### condenser\_api.get\_recent\_trades[](#condenser_api.get_recent_trades)

Returns the most recent trades for the internal HBD:HIVE market. Parameters: `limit:int` up to 1000

`limit` (int)

 

`10`

Queries up to 10 latest trades.

`500`

Queries up to 500 latest trades.

Also see: [market\_history\_api.get\_recent\_trades](/apidefinitions/#market_history_api.get_recent_trades)

##### Query Parameters JSON[](#condenser_api.get_recent_trades-parameter_json)

    [1]
    

##### Expected Response JSON[](#condenser_api.get_recent_trades-expected_response_json)

    [
      {
        "date": "1970-01-01T00:00:00",
        "current_pays": "0.0 HBD",
        "open_pays": "0.0 HIVE"
      }
    ]
    

##### Example `curl`[](#condenser_api.get_recent_trades-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_recent_trades", "params":[10], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_recent_trades", "params":[500], "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF11**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_recovery_request)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-recovery-request)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-recovery-request)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20recovery%20request)**

#### condenser\_api.get\_recovery\_request[](#condenser_api.get_recovery_request)

Returns the recovery request for an account. Parameters: `account:string`

`account` (string)

 

`"hiveio"`

Queries the recovery requests for account named “hiveio”.

Also see: [database\_api.list\_account\_recovery\_requests](/apidefinitions/#database_api.list_account_recovery_requests)

##### Query Parameters JSON[](#condenser_api.get_recovery_request-parameter_json)

    [""]
    

##### Expected Response JSON[](#condenser_api.get_recovery_request-expected_response_json)

    null
    

##### Example `curl`[](#condenser_api.get_recovery_request-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_recovery_request", "params":["hiveio"], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-required-signatures)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-required-signatures)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20required%20signatures)**

#### condenser\_api.get\_required\_signatures[](#condenser_api.get_required_signatures)

This API will take a partially signed transaction and a set of public keys that the owner has the ability to sign for and return the minimal subset of public keys that should add signatures to the transaction. Parameters: `trx:object`; `available_keys:[string]`

Also see: [database\_api.get\_required\_signatures](/apidefinitions/#database_api.get_required_signatures)

##### Query Parameters JSON[](#condenser_api.get_required_signatures-parameter_json)

    [
      {
        "ref_block_num": 0,
        "ref_block_prefix": 0,
        "expiration": "1970-01-01T00:00:00",
        "operations": [],
        "extensions": [],
        "signatures": []
      },
      []
    ]
    

##### Expected Response JSON[](#condenser_api.get_required_signatures-expected_response_json)

    []
    

##### Example `curl`[](#condenser_api.get_required_signatures-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_required_signatures", "params":[{"ref_block_num":1097,"ref_block_prefix":2181793527,"expiration":"2016-03-24T18:00:21","operations":[["pow",{"worker_account":"cloop3","block_id":"00000449f7860b82b4fbe2f317c670e9f01d6d9a","nonce":3899,"work":{"worker":"STM7P5TDnA87Pj9T4mf6YHrhzjC1KbPZpNxLWCcVcHxNYXakpoT4F","input":"ae8e7c677119d22385f8c48026fee7aad7bba693bf788d7f27047f40b47738c0","signature":"1f38fe9a3f9989f84bd94aa5bbc88beaf09b67f825aa4450cf5105d111149ba6db560b582c7dbb026c7fc9c2eb5051815a72b17f6896ed59d3851d9a0f9883ca7a","work":"000e7b209d58f2e64b36e9bf12b999c6c7af168cc3fc41eb7f8a4bf796c174c3"},"props":{"account_creation_fee":{"amount":"100000","precision":3,"nai":"@@000000021"},"maximum_block_size":131072,"hbd_interest_rate":1000}}]],"extensions":[],"signatures":[]},[]], "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF17**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_reward_fund)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-reward-fund)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-reward-fund)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20reward%20fund)**

#### condenser\_api.get\_reward\_fund[](#condenser_api.get_reward_fund)

Returns information about the current reward funds.

Also see: [database\_api.get\_reward\_funds](/apidefinitions/#database_api.get_reward_funds)

##### Query Parameters JSON[](#condenser_api.get_reward_fund-parameter_json)

    ["post"]
    

##### Expected Response JSON[](#condenser_api.get_reward_fund-expected_response_json)

    {
      "id": 0,
      "name": "",
      "reward_balance": "0.000 HIVE",
      "recent_claims": "0",
      "last_update": "1970-01-01T00:00:00",
      "content_constant": "0",
      "percent_curation_rewards": 0,
      "percent_content_rewards": 0,
      "author_reward_curve": "quadratic",
      "curation_reward_curve": "34723648"
    }
    

##### Example `curl`[](#condenser_api.get_reward_fund-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_reward_fund", "params":["post"], "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF14**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_savings_withdraw_from)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-savings-withdraw-from)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-savings-withdraw-from)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20savings%20withdraw)**

#### condenser\_api.get\_savings\_withdraw\_from[](#condenser_api.get_savings_withdraw_from)

Returns savings withdraw from an account. Parameters: `account:string`

`account` (string)

 

`"hiveio"`

Queries the savings withdraw for account named “hiveio”.

Also see: [database\_api.list\_savings\_withdrawals](/apidefinitions/#database_api.list_savings_withdrawals)

##### Query Parameters JSON[](#condenser_api.get_savings_withdraw_from-parameter_json)

    [""]
    

##### Expected Response JSON[](#condenser_api.get_savings_withdraw_from-expected_response_json)

    []
    

##### Example `curl`[](#condenser_api.get_savings_withdraw_from-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_savings_withdraw_from", "params":["hiveio"], "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF14**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_savings_withdraw_to)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-savings-withdraw-to)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-savings-withdraw-to)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20savings%20withdraw)**

#### condenser\_api.get\_savings\_withdraw\_to[](#condenser_api.get_savings_withdraw_to)

Returns the savings withdraw to an account. Parameters: `account:string`

`account` (string)

 

`"hiveio"`

Queries the savings withdraw for account named “hiveio”.

Also see: [database\_api.list\_savings\_withdrawals](/apidefinitions/#database_api.list_savings_withdrawals)

##### Query Parameters JSON[](#condenser_api.get_savings_withdraw_to-parameter_json)

    [""]
    

##### Expected Response JSON[](#condenser_api.get_savings_withdraw_to-expected_response_json)

    []
    

##### Example `curl`[](#condenser_api.get_savings_withdraw_to-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_savings_withdraw_to", "params":["hiveio"], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_ticker)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-ticker)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-ticker)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20ticker)**

#### condenser\_api.get\_ticker[](#condenser_api.get_ticker)

Returns the market ticker for the internal HBD:HIVE market.

Also see: [market\_history\_api.get\_ticker](/apidefinitions/#market_history_api.get_ticker)

##### Query Parameters JSON[](#condenser_api.get_ticker-parameter_json)

    []
    

##### Expected Response JSON[](#condenser_api.get_ticker-expected_response_json)

    {
      "latest": "0.00000000000000000",
      "lowest_ask": "0.00000000000000000",
      "highest_bid": "0.00000000000000000",
      "percent_change": "0.00000000000000000",
      "hive_volume": "0.000 HIVE",
      "hbd_volume": "0.000 HIVE"
    }
    

##### Example `curl`[](#condenser_api.get_ticker-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_ticker", "params":[], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_trade_history)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-trade-history)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-trade-history)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20trade%20history)**

#### condenser\_api.get\_trade\_history[](#condenser_api.get_trade_history)

Returns the trade history for the internal HBD:HIVE market. Parameters: `start:timestamp`; `end:timestamp`; `limit:int` up to 1000

`start` (timestamp)

`end` (timestamp)

`limit` (int)

 

`"2018-01-01T00:00:00"`

`"2018-01-02T00:00:00"`

10

Queries up to 10 trades between January 1st, 2018 and January 2nd, 2018.

Also see: [market\_history\_api.get\_trade\_history](/apidefinitions/#market_history_api.get_trade_history)

##### Query Parameters JSON[](#condenser_api.get_trade_history-parameter_json)

    [
      "1970-01-01T00:00:00",
      "1970-01-01T00:00:00",
      1000
    ]
    

##### Expected Response JSON[](#condenser_api.get_trade_history-expected_response_json)

    [
      {
        "date": "1970-01-01T00:00:00",
        "current_pays": "0.000 HBD",
        "open_pays": "0.000 HIVE"
      }
    ]
    

##### Example `curl`[](#condenser_api.get_trade_history-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_trade_history", "params":["2018-01-01T00:00:00","2018-01-02T00:00:00",10], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_transaction)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-transaction)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-transaction)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20transaction)**

#### condenser\_api.get\_transaction[](#condenser_api.get_transaction)

Returns the details of a transaction based on a transaction id. Parameters: `trx_id:string`

`trx_id` (string)

 

`"6fde0190a97835ea6d9e651293e90c89911f933c"`

Queries for this exact transaction id.

Also see: [account\_history\_api.get\_transaction](/apidefinitions/#account_history_api.get_transaction)

##### Query Parameters JSON[](#condenser_api.get_transaction-parameter_json)

    [""]
    

##### Expected Response JSON[](#condenser_api.get_transaction-expected_response_json)

    {
      "ref_block_num": 0,
      "ref_block_prefix": 0,
      "expiration": "1970-01-01T00:00:00",
      "operations": [],
      "extensions": [],
      "signatures": [],
      "transaction_id": "0000000000000000000000000000000000000000",
      "block_num": 0,
      "transaction_num": 0
    }
    

##### Example `curl`[](#condenser_api.get_transaction-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_transaction", "params":["6fde0190a97835ea6d9e651293e90c89911f933c"], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-transaction-hex)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-transaction-hex)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20transaction%20hex)**

#### condenser\_api.get\_transaction\_hex[](#condenser_api.get_transaction_hex)

Returns a hexdump of the serialized binary form of a transaction.

Also see: [database\_api.get\_transaction\_hex](/apidefinitions/#database_api.get_transaction_hex)

##### Query Parameters JSON[](#condenser_api.get_transaction_hex-parameter_json)

    [
      {
        "ref_block_num": 0,
        "ref_block_prefix": 0,
        "expiration": "1970-01-01T00:00:00",
        "operations": [],
        "extensions": [],
        "signatures": []
      }
    ]
    

##### Expected Response JSON[](#condenser_api.get_transaction_hex-expected_response_json)

    ""
    

##### Example `curl`[](#condenser_api.get_transaction_hex-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_transaction_hex", "params":[{"ref_block_num":1097,"ref_block_prefix":2181793527,"expiration":"2016-03-24T18:00:21","operations":[["pow",{"worker_account":"cloop3","block_id":"00000449f7860b82b4fbe2f317c670e9f01d6d9a","nonce":3899,"work":{"worker":"STM7P5TDnA87Pj9T4mf6YHrhzjC1KbPZpNxLWCcVcHxNYXakpoT4F","input":"ae8e7c677119d22385f8c48026fee7aad7bba693bf788d7f27047f40b47738c0","signature":"1f38fe9a3f9989f84bd94aa5bbc88beaf09b67f825aa4450cf5105d111149ba6db560b582c7dbb026c7fc9c2eb5051815a72b17f6896ed59d3851d9a0f9883ca7a","work":"000e7b209d58f2e64b36e9bf12b999c6c7af168cc3fc41eb7f8a4bf796c174c3"},"props":{"account_creation_fee":{"amount":"100000","precision":3,"nai":"@@000000021"},"maximum_block_size":131072,"hbd_interest_rate":1000}}]],"extensions":[],"signatures":[]}], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_trending_tags)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-trending-tags)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-trending-tags)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/tags)
    
*   **[Related](/search/?q=get%20trending%20tags)**

#### condenser\_api.get\_trending\_tags[](#condenser_api.get_trending_tags)

Returns the list of trending tags. Parameter: `start_tag:string`; `limit:int` up to 100

`tag` (string)

`limit` (int)

 

`null`

100

Queries the top 100 trending tags.

`"hive"`

10

Queries the tags after “hive”, up to 10 tags.

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#condenser_apiget_trending_tags)

##### Query Parameters JSON[](#condenser_api.get_trending_tags-parameter_json)

    ["", 1]
    

##### Expected Response JSON[](#condenser_api.get_trending_tags-expected_response_json)

    [
      {
        "name": "",
        "total_payouts": "0.000 HBD",
        "net_votes": 0,
        "top_posts": 0,
        "comments": 0,
        "trending": ""
      }
    ]
    

##### Example `curl`[](#condenser_api.get_trending_tags-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_trending_tags", "params":[null,100], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_trending_tags", "params":["hive",10], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_version)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-version)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-version)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20version)**

#### condenser\_api.get\_version[](#condenser_api.get_version)

Returns the versions of blockchain, hive, and FC.

Also see: [database\_api.get\_version](/apidefinitions/#database_api.get_version), [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#condenser_apiget_trending_tags)

##### Query Parameters JSON[](#condenser_api.get_version-parameter_json)

    []
    

##### Expected Response JSON[](#condenser_api.get_version-expected_response_json)

    {
      "blockchain_version": "",
      "hive_revision": "",
      "fc_revision": ""
    }
    

##### Example `curl`[](#condenser_api.get_version-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_version", "params":[], "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF17**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_vesting_delegations)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-vesting-delegations)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-vesting-delegations)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/delegations)
    
*   **[Related](/search/?q=get%20vesting%20delegations)**

#### condenser\_api.get\_vesting\_delegations[](#condenser_api.get_vesting_delegations)

Returns the vesting delegations by an account. Parameters: `delegator_account:string`; `start_account:string`; `limit:int` up to 1000

`delegator_account` (string)

`start_account` (string)

`limit` (int)

 

`"hiveio"`

`null`

`10`

Queries up to 10 vesting delegations by “hiveio”.

Also see: [database\_api.list\_vesting\_delegations](/apidefinitions/#database_api.list_vesting_delegations), [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#condenser_apiget_vesting_delegations)

##### Query Parameters JSON[](#condenser_api.get_vesting_delegations-parameter_json)

    ["", "", 1]
    

##### Expected Response JSON[](#condenser_api.get_vesting_delegations-expected_response_json)

    [
      {
        "id": 0,
        "delegator": "",
        "delegatee": "",
        "vesting_shares": "0.000000 VESTS",
        "min_delegation_time": "1970-01-01T00:00:00"
      }
    ]
    

##### Example `curl`[](#condenser_api.get_vesting_delegations-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_vesting_delegations", "params":["hiveio",null,10], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_volume)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-volume)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-volume)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20volume)**

#### condenser\_api.get\_volume[](#condenser_api.get_volume)

Returns the market volume for the past 24 hours.

Also see: [market\_history\_api.get\_volume](/apidefinitions/#market_history_api.get_volume)

##### Query Parameters JSON[](#condenser_api.get_volume-parameter_json)

    []
    

##### Expected Response JSON[](#condenser_api.get_volume-expected_response_json)

    {
      "hive_volume": "0.000 HIVE",
      "hbd_volume": "0.000 HIVE"
    }
    

##### Example `curl`[](#condenser_api.get_volume-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_volume", "params":[], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_withdraw_routes)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-withdraw-routes)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-withdraw-routes)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20withdraw%20routes)**

#### condenser\_api.get\_withdraw\_routes[](#condenser_api.get_withdraw_routes)

Returns the withdraw routes for an account. Parameters: `account:string`; `type:string`

`account` (string)

`type` (string)

 

`"hiveio"`

`"outgoing"`

Queries outgoing withdraw routes by “hiveio”.

`"hiveio"`

`"incoming"`

Queries incoming withdraw routes by “hiveio”.

`"hiveio"`

`"all"`

Queries all withdraw routes by “hiveio”.

Also see: [database\_api.list\_withdraw\_vesting\_routes](/apidefinitions/#database_api.list_withdraw_vesting_routes)

##### Query Parameters JSON[](#condenser_api.get_withdraw_routes-parameter_json)

    ["", ""]
    

##### Expected Response JSON[](#condenser_api.get_withdraw_routes-expected_response_json)

    [
      {
        "id": 0,
        "from_account": "",
        "to_account": "",
        "percent": 0,
        "auto_vest": false
      }
    ]
    

##### Example `curl`[](#condenser_api.get_withdraw_routes-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_withdraw_routes", "params":["hiveio","outgoing"], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_withdraw_routes", "params":["hiveio","incoming"], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_withdraw_routes", "params":["hiveio","all"], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_witness_by_account)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-witness-by-account)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-witness-by-account)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/witnesses)
    
*   **[Related](/search/?q=get%20witness%20account)**

#### condenser\_api.get\_witness\_by\_account[](#condenser_api.get_witness_by_account)

Returns the witness of an account. Parameters: `account:string`

`account` (string)

 

`"hiveio"`

Queries witness account of “hiveio” (of `null` if none exists).

Also see: [database\_api.list\_witnesses](/apidefinitions/#database_api.list_witnesses)

##### Query Parameters JSON[](#condenser_api.get_witness_by_account-parameter_json)

    [""]
    

##### Expected Response JSON[](#condenser_api.get_witness_by_account-expected_response_json)

    {
      "id": 0,
      "owner": "",
      "created": "1970-01-01T00:00:00",
      "url": "",
      "votes": "0",
      "virtual_last_update": "0",
      "virtual_position": "0",
      "virtual_scheduled_time": "0",
      "total_missed": 0,
      "last_aslot": 0,
      "last_confirmed_block_num": 0,
      "pow_worker": 0,
      "signing_key": "",
      "props": {
        "account_creation_fee": "0.000 HIVE",
        "maximum_block_size": 65536,
        "hbd_interest_rate": 0
      },
      "hbd_exchange_rate": {"base": "0.000 HBD", "quote": "0.000 HIVE"},
      "last_hbd_exchange_update": "1970-01-01T00:00:00",
      "last_work": "",
      "running_version": "",
      "hardfork_version_vote": "",
      "hardfork_time_vote": "1970-01-01T00:00:00"
    }
    

##### Example `curl`[](#condenser_api.get_witness_by_account-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_witness_by_account", "params":["hiveio"], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_witness_count)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-witness-count)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-witness-count)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20witness%20count)**

#### condenser\_api.get\_witness\_count[](#condenser_api.get_witness_count)

##### Query Parameters JSON[](#condenser_api.get_witness_count-parameter_json)

    []
    

##### Expected Response JSON[](#condenser_api.get_witness_count-expected_response_json)

    0
    

##### Example `curl`[](#condenser_api.get_witness_count-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_witness_count", "params":[], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_witness_schedule)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-witness-schedule)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-witness-schedule)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20witness%20schedule)**

#### condenser\_api.get\_witness\_schedule[](#condenser_api.get_witness_schedule)

Returns the current witness schedule.

Also see: [database\_api.get\_witness\_schedule](/apidefinitions/#database_api.get_witness_schedule)

##### Query Parameters JSON[](#condenser_api.get_witness_schedule-parameter_json)

    []
    

##### Expected Response JSON[](#condenser_api.get_witness_schedule-expected_response_json)

    {
      "id": 0,
      "current_virtual_time": "0",
      "next_shuffle_block_num": 1,
      "current_shuffled_witnesses": [],
      "num_scheduled_witnesses": 1,
      "top19_weight": 1,
      "timeshare_weight": 5,
      "miner_weight": 1,
      "witness_pay_normalization_factor": 25,
      "median_props": {
        "account_creation_fee": "0.000 HIVE",
        "maximum_block_size": 131072,
        "hbd_interest_rate": 1000
      },
      "majority_version": "0.0.0",
      "max_voted_witnesses": 19,
      "max_miner_witnesses": 1,
      "max_runner_witnesses": 1,
      "hardfork_required_witnesses": 17
    }
    

##### Example `curl`[](#condenser_api.get_witness_schedule-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_witness_schedule", "params":[], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_witnesses)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-witnesses)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-witnesses)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/witnesses)
    
*   **[Related](/search/?q=get%20witnesses)**

#### condenser\_api.get\_witnesses[](#condenser_api.get_witnesses)

Returns current witnesses.

Also see: [database\_api.list\_witnesses](/apidefinitions/#database_api.list_witnesses)

##### Query Parameters JSON[](#condenser_api.get_witnesses-parameter_json)

    [[0]]
    

##### Expected Response JSON[](#condenser_api.get_witnesses-expected_response_json)

    []
    

##### Example `curl`[](#condenser_api.get_witnesses-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_witnesses", "params":[[28]], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_witnesses_by_vote)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-witnesses-by-vote)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-witnesses-by-vote)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/witnesses)
    
*   **[Related](/search/?q=get%20witnesses%20vote)**

#### condenser\_api.get\_witnesses\_by\_vote[](#condenser_api.get_witnesses_by_vote)

Returns current witnesses by vote. Parameters: `start_name:string`; `limit:int` up to 1000

`account` (string)

`limit` (int)

 

`null`

`21`

Queries top 21 witness votes.

`"a"`

`1`

Queries top 10 witness votes starting with “a”.

Also see: [database\_api.list\_witnesses](/apidefinitions/#database_api.list_witnesses)

##### Query Parameters JSON[](#condenser_api.get_witnesses_by_vote-parameter_json)

    ["", 1000]
    

##### Expected Response JSON[](#condenser_api.get_witnesses_by_vote-expected_response_json)

    []
    

##### Example `curl`[](#condenser_api.get_witnesses_by_vote-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_witnesses_by_vote", "params":[null, 21], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.get_witnesses_by_vote", "params":["a", 1], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=lookup_account_names)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#lookup-account-names)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#lookup-account-names)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=lookup%20account%20names)**

#### condenser\_api.lookup\_account\_names[](#condenser_api.lookup_account_names)

Looks up account names. Parameters: `accounts:[string]`; `delayed_votes_active:boolean`

Also see: [database\_api.find\_accounts](/apidefinitions/#database_api.find_accounts)

##### Query Parameters JSON[](#condenser_api.lookup_account_names-parameter_json)

    [["hiveio", true]]
    

##### Expected Response JSON[](#condenser_api.lookup_account_names-expected_response_json)

    {
      "id": 1370484,
      "name": "hiveio",
      "owner": {
        "weight_threshold": 1,
        "account_auths": [],
        "key_auths": [
          [
            "STM65PUAPA4yC4RgPtGgsPupxT6yJtMhmT5JHFdsT3uoCbR8WJ25s",
            1
          ]
        ]
      },
      "active": {
        "weight_threshold": 1,
        "account_auths": [],
        "key_auths": [
          [
            "STM69zfrFGnZtU3gWFWpQJ6GhND1nz7TJsKBTjcWfebS1JzBEweQy",
            1
          ]
        ]
      },
      "posting": {
        "weight_threshold": 1,
        "account_auths": [["threespeak", 1], ["vimm.app", 1]],
        "key_auths": [
          [
            "STM6vJmrwaX5TjgTS9dPH8KsArso5m91fVodJvv91j7G765wqcNM9",
            1
          ]
        ]
      },
      "memo_key": "STM7wrsg1BZogeK7X3eG4ivxmLaH69FomR8rLkBbepb3z3hm5SbXu",
      "json_metadata": "",
      "posting_json_metadata": "{\"profile\":{\"pinned\":\"none\",\"version\":2,\"website\":\"hive.io\",\"profile_image\":\"https://files.peakd.com/file/peakd-hive/hiveio/Jp2YHc6Q-hive-logo.png\",\"cover_image\":\"https://files.peakd.com/file/peakd-hive/hiveio/Xe1TcEBi-hive-banner.png\"}}",
      "proxy": "",
      "last_owner_update": "1970-01-01T00:00:00",
      "last_account_update": "2020-11-12T01:20:48",
      "created": "2020-03-06T12:22:48",
      "mined": false,
      "recovery_account": "steempeak",
      "last_account_recovery": "1970-01-01T00:00:00",
      "reset_account": "null",
      "comment_count": 0,
      "lifetime_vote_count": 0,
      "post_count": 31,
      "can_vote": true,
      "voting_manabar": {
        "current_mana": "598442432741",
        "last_update_time": 1591297380
      },
      "downvote_manabar": {
        "current_mana": "149610608184",
        "last_update_time": 1591297380
      },
      "voting_power": 0,
      "balance": "11.682 HIVE",
      "savings_balance": "0.000 HIVE",
      "hbd_balance": "43.575 HBD",
      "hbd_seconds": "0",
      "hbd_seconds_last_update": "2020-10-21T02:45:12",
      "hbd_last_interest_payment": "2020-10-21T02:45:12",
      "savings_hbd_balance": "0.000 HBD",
      "savings_hbd_seconds": "0",
      "savings_hbd_seconds_last_update": "1970-01-01T00:00:00",
      "savings_hbd_last_interest_payment": "1970-01-01T00:00:00",
      "savings_withdraw_requests": 0,
      "reward_hbd_balance": "0.000 HBD",
      "reward_hive_balance": "0.000 HIVE",
      "reward_vesting_balance": "0.000000 VESTS",
      "reward_vesting_hive": "0.000 HIVE",
      "vesting_shares": "598442.432741 VESTS",
      "delegated_vesting_shares": "0.000000 VESTS",
      "received_vesting_shares": "0.000000 VESTS",
      "vesting_withdraw_rate": "0.000000 VESTS",
      "post_voting_power": "598442.432741 VESTS",
      "next_vesting_withdrawal": "1969-12-31T23:59:59",
      "withdrawn": 0,
      "to_withdraw": 0,
      "withdraw_routes": 0,
      "pending_transfers": 0,
      "curation_rewards": 0,
      "posting_rewards": 604589,
      "proxied_vsf_votes": [0, 0, 0, 0],
      "witnesses_voted_for": 0,
      "last_post": "2021-03-23T18:05:48",
      "last_root_post": "2021-03-23T18:05:48",
      "last_vote_time": "1970-01-01T00:00:00",
      "post_bandwidth": 0,
      "pending_claimed_accounts": 0,
      "delayed_votes": [
        {
          "time": "2021-02-24T05:08:21",
          "val": "11550765516955"
        },
        {
          "time": "2021-02-26T15:46:06",
          "val": "633465684569"
        },
        {
          "time": "2021-03-07T17:54:39",
          "val": "1000000037683"
        },
        {
          "time": "2021-03-16T05:54:33",
          "val": "999978763511"
        },
        {
          "time": "2021-03-18T06:06:00",
          "val": "1000000171317"
        }
      ],
      "vesting_balance": "0.000 HIVE",
      "reputation": "88826789432105",
      "transfer_history": [],
      "market_history": [],
      "post_history": [],
      "vote_history": [],
      "other_history": [],
      "witness_votes": [],
      "tags_usage": [],
      "guest_bloggers": []
    }
    

##### Example `curl`[](#condenser_api.lookup_account_names-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.lookup_account_names", "params":[["hiveio"]], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.lookup_account_names", "params":[["hiveio"], false], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=lookup_accounts)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#lookup-accounts)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#lookup-accounts)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=lookup%20accounts)**

#### condenser\_api.lookup\_accounts[](#condenser_api.lookup_accounts)

Looks up accounts starting with name. Parameters`lower_bound_name:string`; `limit:int` up to 1000

`lower_bound_name` (string)

`limit` (int)

 

`"a"`

10

Queries up to 10 accounts that start with “a”.

Also see: [database\_api.list\_accounts](/apidefinitions/#database_api.list_accounts)

##### Query Parameters JSON[](#condenser_api.lookup_accounts-parameter_json)

    ["", 1]
    

##### Expected Response JSON[](#condenser_api.lookup_accounts-expected_response_json)

    []
    

##### Example `curl`[](#condenser_api.lookup_accounts-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.lookup_accounts", "params":["a",10], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=lookup_witness_accounts)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#lookup-witness-accounts)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#lookup-witness-accounts)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/witnesses)
    
*   **[Related](/search/?q=lookup%20witness%20accounts)**

#### condenser\_api.lookup\_witness\_accounts[](#condenser_api.lookup_witness_accounts)

Looks up witness accounts starting with name. Parameters: `lower_bound_name:string`; `limit:int` up to 1000

`lower_bound_name` (string)

`limit` (int)

 

`"a"`

10

Queries up to 10 witnesses that start with “a”.

Also see: [database\_api.list\_witnesses](/apidefinitions/#database_api.list_witnesses)

##### Query Parameters JSON[](#condenser_api.lookup_witness_accounts-parameter_json)

    ["", 1]
    

##### Expected Response JSON[](#condenser_api.lookup_witness_accounts-expected_response_json)

    []
    

##### Example `curl`[](#condenser_api.lookup_witness_accounts-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.lookup_witness_accounts", "params":["a",10], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#verify-authority)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#verify-authority)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=verify%20authority)**

#### condenser\_api.verify\_authority[](#condenser_api.verify_authority)

Returns true if the transaction has all of the required signatures.

Also see: [database\_api.verify\_authority](/apidefinitions/#database_api.verify_authority)

##### Query Parameters JSON[](#condenser_api.verify_authority-parameter_json)

    [
      {
        "ref_block_num": 0,
        "ref_block_prefix": 0,
        "expiration": "1970-01-01T00:00:00",
        "operations": [],
        "extensions": [],
        "signatures": []
      }
    ]
    

##### Expected Response JSON[](#condenser_api.verify_authority-expected_response_json)

    false
    

##### Example `curl`[](#condenser_api.verify_authority-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.verify_authority", "params":[{"ref_block_num":1097,"ref_block_prefix":2181793527,"expiration":"2016-03-24T18:00:21","operations":[["pow",{"worker_account":"cloop3","block_id":"00000449f7860b82b4fbe2f317c670e9f01d6d9a","nonce":3899,"work":{"worker":"STM7P5TDnA87Pj9T4mf6YHrhzjC1KbPZpNxLWCcVcHxNYXakpoT4F","input":"ae8e7c677119d22385f8c48026fee7aad7bba693bf788d7f27047f40b47738c0","signature":"1f38fe9a3f9989f84bd94aa5bbc88beaf09b67f825aa4450cf5105d111149ba6db560b582c7dbb026c7fc9c2eb5051815a72b17f6896ed59d3851d9a0f9883ca7a","work":"000e7b209d58f2e64b36e9bf12b999c6c7af168cc3fc41eb7f8a4bf796c174c3"},"props":{"account_creation_fee":{"amount":"100000","precision":3,"nai":"@@000000021"},"maximum_block_size":131072,"hbd_interest_rate":1000}}]],"extensions":[],"signatures":[]}], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=find_proposals)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/proposals)
    
*   **[Related](/search/?q=find%20proposals)**

#### condenser\_api.find\_proposals[](#condenser_api.find_proposals)

Finds proposals by `proposal.id` (not `proposal.proposal_id`).

Also see: [database\_api.find\_proposals](/apidefinitions/#database_api.find_proposals)

##### Query Parameters JSON[](#condenser_api.find_proposals-parameter_json)

    [0]
    

##### Expected Response JSON[](#condenser_api.find_proposals-expected_response_json)

    [
      {
        "id": 0,
        "proposal_id": "139924505899904",
        "creator": "alice",
        "receiver": "bob",
        "start_date": "2019-07-01T00:00:00",
        "end_date": "2019-08-01T23:59:59",
        "daily_pay": "4800.000 HBD",
        "subject": "My Proposal",
        "permlink": "creator-proposal-permlink",
        "total_votes": "77351826710",
        "status": "active"
      }
    ]
    

##### Example `curl`[](#condenser_api.find_proposals-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.find_proposals", "params":[[0]], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=list_proposal_votes)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/proposalsapprovals)
    
*   **[Related](/search/?q=list%20proposal%20votes)**

#### condenser\_api.list\_proposal\_votes[](#condenser_api.list_proposal_votes)

Returns all proposal votes, starting with the specified voter or `proposal.id`. Parameters: `start:array`; `limit:int`; `order:string`; `order_direction:string`; `status:string`

*   `start` depends on `order` (see below)
    *   `voter` - voter of the proposal (account name string)
    *   `proposal.id` - id the proposal (int)
*   `limit` is up to 1000.
*   `order` can be one of:
    *   `by_voter_proposal` - order by proposal voter
    *   `by_proposal_voter` - order by `proposal.id`
*   `order_direction` can be one of:
    *   `ascending`
    *   `descending`
*   `status`
    *   `all`
    *   `inactive`
    *   `active`
    *   `expired`
    *   `votable`

`start` (array)

`limit` (int)

`order` (string)

`order_direction` (string)

`status` (string)

 

`["alice"]`

10

`by_voter_proposal`

`ascending`

`active`

list 10 proposals with active status, ordered by voter, ascending

`[10]`

1000

`by_proposal_voter`

`ascending`

`votable`

list 1000 votes on proposal 10, ordered by `proposal.id`, ascending

Also see: [database\_api.list\_proposals](/apidefinitions/#database_api.list_proposal_votes)

##### Query Parameters JSON[](#condenser_api.list_proposal_votes-parameter_json)

    [[], 0, "by_name", "ascending", "all"]
    

##### Expected Response JSON[](#condenser_api.list_proposal_votes-expected_response_json)

    [
      {
        "id": 0,
        "voter": "charlie",
        "proposal": {
          "id": 0,
          "proposal_id": 0,
          "creator": "alice",
          "receiver": "bob",
          "start_date": "2019-07-01T00:00:00",
          "end_date": "2019-08-01T23:59:59",
          "daily_pay": {
            "amount": "4800000",
            "precision": 3,
            "nai": "@@000000013"
          },
          "subject": "My Proposal",
          "permlink": "creator-proposal-permlink",
          "total_votes": "77351826710",
          "status": "active"
        }
      }
    ]
    

##### Example `curl`[](#condenser_api.list_proposal_votes-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.list_proposal_votes", "params":[[""], 10, "by_voter_proposal", "ascending", "active"], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.list_proposal_votes", "params":[[0], 10, "by_proposal_voter", "ascending", "active"], "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=list_proposals)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/proposals)
    
*   **[Related](/search/?q=list%20proposals)**

#### condenser\_api.list\_proposals[](#condenser_api.list_proposals)

Returns all proposals, starting with the specified creator or start date. Parameters: `start:array`; `limit:int`; `order:string`; `order_direction:string`; `status:string`

*   `start` depends on `order` (see below)
    *   `creator` - creator of the proposal (account name string)
    *   `start_date` - start date of the proposal (date string)
    *   `end_date` - end date of the proposal (date string)
    *   `total_votes` - total votes of the proposal (int)
*   `limit` is up to 1000.
*   `order` can be one of:
    *   `by_creator` - order by proposal creator
    *   `by_start_date` - order by proposal start date
    *   `by_end_date` - order by proposal end date
    *   `by_total_votes` - order by proposal total votes
*   `order_direction` can be one of:
    *   `ascending`
    *   `descending`
*   `status`
    *   `all`
    *   `inactive`
    *   `active`
    *   `expired`
    *   `votable`

`start` (array)

`limit` (int)

`order` (string)

`order_direction` (string)

`status` (string)

 

`[""]`

10

`by_creator`

`ascending`

`active`

list 10 proposals with active status, ordered by creator, ascending

`["2019-08-07T16:54:03"]`

1000

`by_start_date`

`ascending`

`inactive`

list 1000 proposals with inactive status, ordered by start date, ascending, since 2019-08-07T16:54:03

`["a"]`

1

`by_creator`

`ascending`

`expired`

list 1 proposal with expired status, ordered by creator, ascending, by accounts starting with “a”

`["alice"]`

10

`by_creator`

`ascending`

`all`

list 10 proposals with any status, ordered by creator, ascending, by alice

`[""]`

1000

`by_creator`

`ascending`

`votable`

list 1000 votable proposals, ordered by creator, ascending

`[10]`

1000

`by_total_votes`

`ascending`

`votable`

list 1000 votable proposals, ordered by creator, ascending, having at least 10 votes

Also see: [datbase\_api.list\_proposals](/apidefinitions/#database_api.list_proposals)

##### Query Parameters JSON[](#condenser_api.list_proposals-parameter_json)

    [[], 0, "by_name", "ascending", "all"]
    

##### Expected Response JSON[](#condenser_api.list_proposals-expected_response_json)

    [
      {
        "id": 0,
        "proposal_id": "1103806595072",
        "creator": "alice",
        "receiver": "bob",
        "start_date": "2019-07-01T00:00:00",
        "end_date": "2019-08-01T23:59:59",
        "daily_pay": "4800.000 HBD",
        "subject": "My Proposal",
        "permlink": "creator-proposal-permlink",
        "total_votes": "77351826710",
        "status": "active"
      }
    ]
    

##### Example `curl`[](#condenser_api.list_proposals-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.list_proposals", "params":[[""], 10, "by_creator", "ascending", "active"], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.list_proposals", "params":[["2019-08-07T16:54:03"], 1000, "order_direction": "ascending", "inactive"], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.list_proposals", "params":[["a"], 1, "by_creator", "ascending", "expired"], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.list_proposals", "params":[["alice"], 10, "by_creator", "ascending", "all"], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.list_proposals", "params":[[""], 1000, "by_creator", "ascending", "votable"], "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.list_proposals", "params":[[10], 1000, "by_total_votes", "ascending", "votable"], "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF25**
*   **[Related](/search/?q=known%20transaction)**

#### condenser\_api.is\_known\_transaction[](#condenser_api.is_known_transaction)

Only return true _if_ the transaction has not expired or been invalidated. If this method is called with a VERY old transaction we will return false, use `account_history_api.get_transaction`.

Also see: [transaction\_status\_api.find\_transaction](/apidefinitions/#transaction_status_api.find_transaction), [account\_history\_api.get\_transaction](/apidefinitions/#account_history_api.get_transaction)

##### Query Parameters JSON[](#condenser_api.is_known_transaction-parameter_json)

    ["0000000000000000000000000000000000000000"]
    

##### Expected Response JSON[](#condenser_api.is_known_transaction-expected_response_json)

    false
    

##### Example `curl`[](#condenser_api.is_known_transaction-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.is_known_transaction", "params":["0000000000000000000000000000000000000000"]}, "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF25**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_collateralized_conversion_requests)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/-/blob/master/doc/README.md#collateralized-convert)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txcollateralizedconverts-hf25)
    
*   **[Related](/search/?q=get%20collateralized%20conversion%20requests)**

#### condenser\_api.get\_collateralized\_conversion\_requests[](#condenser_api.get_collateralized_conversion_requests)

Returns objects corresponding with `collateralized_convert` operations.

##### Query Parameters JSON[](#condenser_api.get_collateralized_conversion_requests-parameter_json)

    []
    

##### Expected Response JSON[](#condenser_api.get_collateralized_conversion_requests-expected_response_json)

    []
    

* * *

*   **Since: HF25**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=find_recurrent_transfers)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txrecurrenttransfers-hf25)
    
*   **[Related](/search/?q=find%20recurrent%20transfers)**

#### condenser\_api.find\_recurrent\_transfers[](#condenser_api.find_recurrent_transfers)

Finds transfers of any liquid asset every fixed amount of time from one account to another.

Also see: [recurrent\_transfer\_operation](/apidefinitions/#broadcast_ops_recurrent_transfer)

##### Query Parameters JSON[](#condenser_api.find_recurrent_transfers-parameter_json)

    [""]
    

##### Expected Response JSON[](#condenser_api.find_recurrent_transfers-expected_response_json)

    [
      {
        "id": 3,
        "trigger_date": "2021-07-02T18:11:51",
        "from": "alice",
        "to": "bob",
        "amount": {
          "amount": "1000",
          "precision": 3,
          "nai": "@@000000021"
        },
        "memo": "Payroll",
        "recurrence": 26,
        "consecutive_failures": 0,
        "remaining_executions": 3
      }
    ]
    

##### Example `curl`[](#condenser_api.find_recurrent_transfers-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.find_recurrent_transfers", "params":["alice"], "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF26**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=find_rc_accounts)
    
*   **[Related](/search/?q=find%20rc%20accounts)**

#### condenser\_api.find\_rc\_accounts[](#condenser_api.find_rc_accounts)

Returns the available resource credits of accounts.

##### Query Parameters JSON[](#condenser_api.find_rc_accounts-parameter_json)

    []
    

##### Expected Response JSON[](#condenser_api.find_rc_accounts-expected_response_json)

    [
      {
        "account": "alice",
        "delegated_rc": 0,
        "max_rc": 135630143570,
        "max_rc_creation_adjustment": "2020.748973 VESTS",
        "rc_manabar": {
          "current_mana": 135375191366,
          "last_update_time": 1550731380
        },
        "received_delegated_rc": 0
      },
      {
        "account": "demo",
        "delegated_rc": 0,
        "max_rc": 50966868081,
        "max_rc_creation_adjustment": "2020.748973 VESTS",
        "rc_manabar": {
          "current_mana": 50966868081,
          "last_update_time": 1715912571
        },
        "received_delegated_rc": 6000000000
      }
    ]
    

##### Example `curl`[](#condenser_api.find_rc_accounts-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.find_rc_accounts", "params":[["alice","demo"]], "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF26**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=list_rc_accounts)
    
*   **[Related](/search/?q=list%20rc%20accounts)**

#### condenser\_api.list\_rc\_accounts[](#condenser_api.list_rc_accounts)

Find accounts and their RC delegations

##### Query Parameters JSON[](#condenser_api.list_rc_accounts-parameter_json)

    []
    

##### Expected Response JSON[](#condenser_api.list_rc_accounts-expected_response_json)

    [
      {
        "account": "ecency",
        "delegated_rc": 2065000000000,
        "max_rc": 7671956433568695,
        "max_rc_creation_adjustment": "5851.327807 VESTS",
        "rc_manabar": {
          "current_mana": 3221987144996,
          "last_update_time": 1716194709
        },
        "received_delegated_rc": 4484642315668049
      },
      {
        "account": "ecency-987",
        "delegated_rc": 0,
        "max_rc": 5568323871,
        "max_rc_creation_adjustment": "5568.323871 VESTS",
        "rc_manabar": {
          "current_mana": 5568323871,
          "last_update_time": 1637136366
        },
        "received_delegated_rc": 0
      }
    ]
    

##### Example `curl`[](#condenser_api.list_rc_accounts-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.list_rc_accounts", "params":["ecency",10], "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF26**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=list_rc_direct_delegations)
    
*   **[Related](/search/?q=list%20rc%20direct%20delegations)**

#### condenser\_api.list\_rc\_direct\_delegations[](#condenser_api.list_rc_direct_delegations)

Get list of “from” “to” which account how much RC was delegated.

##### Query Parameters JSON[](#condenser_api.list_rc_direct_delegations-parameter_json)

    []
    

##### Expected Response JSON[](#condenser_api.list_rc_direct_delegations-expected_response_json)

    [
      {
        "delegated_rc": 15000000000,
        "from": "ecency",
        "to": "raitakun501"
      },
      {
        "delegated_rc": 15000000000,
        "from": "ecency",
        "to": "vivianemitola"
      }
    ]
    

##### Example `curl`[](#condenser_api.list_rc_direct_delegations-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"condenser_api.list_rc_direct_delegations", "params":[["ecency",""],2], "id":1}' https://api.hive.blog
    

* * *

### Database API

Methods:

*   [find\_account\_recovery\_requests](#database_api.find_account_recovery_requests)
*   [find\_accounts](#database_api.find_accounts)
*   [find\_change\_recovery\_account\_requests](#database_api.find_change_recovery_account_requests)
*   [find\_collateralized\_conversion\_requests](#database_api.find_collateralized_conversion_requests)
*   [find\_comments](#database_api.find_comments)
*   [find\_decline\_voting\_rights\_requests](#database_api.find_decline_voting_rights_requests)
*   [find\_escrows](#database_api.find_escrows)
*   [find\_hbd\_conversion\_requests](#database_api.find_hbd_conversion_requests)
*   [find\_limit\_orders](#database_api.find_limit_orders)
*   [find\_owner\_histories](#database_api.find_owner_histories)
*   [find\_proposals](#database_api.find_proposals)
*   [find\_recurrent\_transfers](#database_api.find_recurrent_transfers)
*   [find\_savings\_withdrawals](#database_api.find_savings_withdrawals)
*   [find\_vesting\_delegation\_expirations](#database_api.find_vesting_delegation_expirations)
*   [find\_vesting\_delegations](#database_api.find_vesting_delegations)
*   [find\_votes](#database_api.find_votes)
*   [find\_withdraw\_vesting\_routes](#database_api.find_withdraw_vesting_routes)
*   [find\_witnesses](#database_api.find_witnesses)
*   [get\_active\_witnesses](#database_api.get_active_witnesses)
*   [get\_comment\_pending\_payouts](#database_api.get_comment_pending_payouts)
*   [get\_config](#database_api.get_config)
*   [get\_current\_price\_feed](#database_api.get_current_price_feed)
*   [get\_dynamic\_global\_properties](#database_api.get_dynamic_global_properties)
*   [get\_feed\_history](#database_api.get_feed_history)
*   [get\_hardfork\_properties](#database_api.get_hardfork_properties)
*   [get\_order\_book](#database_api.get_order_book)
*   [get\_potential\_signatures](#database_api.get_potential_signatures)
*   [get\_required\_signatures](#database_api.get_required_signatures)
*   [get\_reward\_funds](#database_api.get_reward_funds)
*   [get\_transaction\_hex](#database_api.get_transaction_hex)
*   [get\_version](#database_api.get_version)
*   [get\_witness\_schedule](#database_api.get_witness_schedule)
*   [is\_known\_transaction](#database_api.is_known_transaction)
*   [list\_account\_recovery\_requests](#database_api.list_account_recovery_requests)
*   [list\_accounts](#database_api.list_accounts)
*   [list\_change\_recovery\_account\_requests](#database_api.list_change_recovery_account_requests)
*   [list\_collateralized\_conversion\_requests](#database_api.list_collateralized_conversion_requests)
*   [list\_comments](#database_api.list_comments)
*   [list\_decline\_voting\_rights\_requests](#database_api.list_decline_voting_rights_requests)
*   [list\_escrows](#database_api.list_escrows)
*   [list\_hbd\_conversion\_requests](#database_api.list_hbd_conversion_requests)
*   [list\_limit\_orders](#database_api.list_limit_orders)
*   [list\_owner\_histories](#database_api.list_owner_histories)
*   [list\_proposal\_votes](#database_api.list_proposal_votes)
*   [list\_proposals](#database_api.list_proposals)
*   [list\_savings\_withdrawals](#database_api.list_savings_withdrawals)
*   [list\_vesting\_delegation\_expirations](#database_api.list_vesting_delegation_expirations)
*   [list\_vesting\_delegations](#database_api.list_vesting_delegations)
*   [list\_votes](#database_api.list_votes)
*   [list\_withdraw\_vesting\_routes](#database_api.list_withdraw_vesting_routes)
*   [list\_witness\_votes](#database_api.list_witness_votes)
*   [list\_witnesses](#database_api.list_witnesses)
*   [verify\_account\_authority](#database_api.verify_account_authority)
*   [verify\_authority](#database_api.verify_authority)
*   [verify\_signatures](#database_api.verify_signatures)

Used to query information about accounts, transactions, and blockchain data.

To enable this API for `hived`, the following is required in `config.ini` by specifying:

    plugin = database_api
    

**These AppBase API methods are still under development and subject to change.**

*   **Since: HF11**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=find_account_recovery_requests)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-recovery-request)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-recovery-request)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=find%20account%20recovery%20requests)**

#### database\_api.find\_account\_recovery\_requests[](#database_api.find_account_recovery_requests)

Returns a list of account recovery requests. Parameters: `account:string`

`account` (string)

 

`"hiveio"`

Queries the recovery requests for account named “hiveio”.

##### Query Parameters JSON[](#database_api.find_account_recovery_requests-parameter_json)

    {"accounts": []}
    

##### Expected Response JSON[](#database_api.find_account_recovery_requests-expected_response_json)

    {"requests": []}
    

##### Example `curl`[](#database_api.find_account_recovery_requests-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.find_account_recovery_requests", "params": {"accounts":["hiveio"]}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=find_accounts)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-accounts)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.blockchain.html#beem.blockchain.Blockchain.get_all_accounts)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/accounts)
    
*   **[Related](/search/?q=find%20accounts)**

#### database\_api.find\_accounts[](#database_api.find_accounts)

Returns accounts, queried by name. Parameters: `account:string array`; `delayed_votes_active:boolean`

`account` (string array)

`delayed_votes_active` (boolean)

 

`["hiveio"]`

 

Queries for account named “hiveio”.

`["hiveio", "alice"]`

false

Queries for accounts named “hiveio” and “alice” with `delayed_votes` hidden.

##### Query Parameters JSON[](#database_api.find_accounts-parameter_json)

    {"accounts": [], "delayed_votes_active": true}
    

##### Expected Response JSON[](#database_api.find_accounts-expected_response_json)

    {
      "accounts": [
        {
          "id": 1370484,
          "name": "hiveio",
          "owner": {
            "weight_threshold": 1,
            "account_auths": [],
            "key_auths": [
              [
                "STM65PUAPA4yC4RgPtGgsPupxT6yJtMhmT5JHFdsT3uoCbR8WJ25s",
                1
              ]
            ]
          },
          "active": {
            "weight_threshold": 1,
            "account_auths": [],
            "key_auths": [
              [
                "STM69zfrFGnZtU3gWFWpQJ6GhND1nz7TJsKBTjcWfebS1JzBEweQy",
                1
              ]
            ]
          },
          "posting": {
            "weight_threshold": 1,
            "account_auths": [["threespeak", 1], ["vimm.app", 1]],
            "key_auths": [
              [
                "STM6vJmrwaX5TjgTS9dPH8KsArso5m91fVodJvv91j7G765wqcNM9",
                1
              ]
            ]
          },
          "memo_key": "STM7wrsg1BZogeK7X3eG4ivxmLaH69FomR8rLkBbepb3z3hm5SbXu",
          "json_metadata": "",
          "posting_json_metadata": "{\"profile\":{\"pinned\":\"none\",\"version\":2,\"website\":\"hive.io\",\"profile_image\":\"https://files.peakd.com/file/peakd-hive/hiveio/Jp2YHc6Q-hive-logo.png\",\"cover_image\":\"https://files.peakd.com/file/peakd-hive/hiveio/Xe1TcEBi-hive-banner.png\"}}",
          "proxy": "",
          "last_owner_update": "1970-01-01T00:00:00",
          "last_account_update": "2020-11-12T01:20:48",
          "created": "2020-03-06T12:22:48",
          "mined": false,
          "recovery_account": "steempeak",
          "last_account_recovery": "1970-01-01T00:00:00",
          "reset_account": "null",
          "comment_count": 0,
          "lifetime_vote_count": 0,
          "post_count": 31,
          "can_vote": true,
          "voting_manabar": {
            "current_mana": "598442432741",
            "last_update_time": 1591297380
          },
          "downvote_manabar": {
            "current_mana": "149610608184",
            "last_update_time": 1591297380
          },
          "balance": {
            "amount": "11682",
            "precision": 3,
            "nai": "@@000000021"
          },
          "savings_balance": {
            "amount": "0",
            "precision": 3,
            "nai": "@@000000021"
          },
          "hbd_balance": {
            "amount": "43575",
            "precision": 3,
            "nai": "@@000000013"
          },
          "hbd_seconds": "0",
          "hbd_seconds_last_update": "2020-10-21T02:45:12",
          "hbd_last_interest_payment": "2020-10-21T02:45:12",
          "savings_hbd_balance": {
            "amount": "0",
            "precision": 3,
            "nai": "@@000000013"
          },
          "savings_hbd_seconds": "0",
          "savings_hbd_seconds_last_update": "1970-01-01T00:00:00",
          "savings_hbd_last_interest_payment": "1970-01-01T00:00:00",
          "savings_withdraw_requests": 0,
          "reward_hbd_balance": {
            "amount": "0",
            "precision": 3,
            "nai": "@@000000013"
          },
          "reward_hive_balance": {
            "amount": "0",
            "precision": 3,
            "nai": "@@000000021"
          },
          "reward_vesting_balance": {
            "amount": "0",
            "precision": 6,
            "nai": "@@000000037"
          },
          "reward_vesting_hive": {
            "amount": "0",
            "precision": 3,
            "nai": "@@000000021"
          },
          "vesting_shares": {
            "amount": "598442432741",
            "precision": 6,
            "nai": "@@000000037"
          },
          "delegated_vesting_shares": {
            "amount": "0",
            "precision": 6,
            "nai": "@@000000037"
          },
          "received_vesting_shares": {
            "amount": "0",
            "precision": 6,
            "nai": "@@000000037"
          },
          "vesting_withdraw_rate": {
            "amount": "0",
            "precision": 6,
            "nai": "@@000000037"
          },
          "post_voting_power": {
            "amount": "598442432741",
            "precision": 6,
            "nai": "@@000000037"
          },
          "next_vesting_withdrawal": "1969-12-31T23:59:59",
          "withdrawn": 0,
          "to_withdraw": 0,
          "withdraw_routes": 0,
          "pending_transfers": 0,
          "curation_rewards": 0,
          "posting_rewards": 604589,
          "proxied_vsf_votes": [0, 0, 0, 0],
          "witnesses_voted_for": 0,
          "last_post": "2021-03-23T18:05:48",
          "last_root_post": "2021-03-23T18:05:48",
          "last_post_edit": "2021-03-23T18:05:48",
          "last_vote_time": "1970-01-01T00:00:00",
          "post_bandwidth": 0,
          "pending_claimed_accounts": 0,
          "is_smt": false,
          "delayed_votes": [
            {
              "time": "2021-02-24T05:08:21",
              "val": "11550765516955"
            },
            {
              "time": "2021-02-26T15:46:06",
              "val": "633465684569"
            },
            {
              "time": "2021-03-07T17:54:39",
              "val": "1000000037683"
            },
            {
              "time": "2021-03-16T05:54:33",
              "val": "999978763511"
            },
            {
              "time": "2021-03-18T06:06:00",
              "val": "1000000171317"
            }
          ]
        }
      ]
    }
    

##### Example `curl`[](#database_api.find_accounts-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.find_accounts", "params": {"accounts":["hiveio"]}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.find_accounts", "params": {"accounts":["hiveio", "alice"], "delayed_votes_active": false}, "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF11**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=find_change_recovery_account_requests)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-recovery-request)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.blockchain.html#beem.blockchain.Blockchain.find_change_recovery_account_requests)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=find%20change%20recovery%20account%20requests)**

#### database\_api.find\_change\_recovery\_account\_requests[](#database_api.find_change_recovery_account_requests)

Returns a list of requests to change the recovery account. Parameters: `account:array`

`account` (array)

 

`["hiveio"]`

Queries the recovery requests for account named “hiveio”.

##### Query Parameters JSON[](#database_api.find_change_recovery_account_requests-parameter_json)

    {"accounts": []}
    

##### Expected Response JSON[](#database_api.find_change_recovery_account_requests-expected_response_json)

    {
      "requests": [
        {
          "id": 0,
          "account_to_recover": "",
          "recovery_account": "",
          "effective_on": "2020-01-08T00:45:18"
        }
      ]
    }
    

##### Example `curl`[](#database_api.find_change_recovery_account_requests-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.find_change_recovery_account_requests", "params": {"accounts":["hiveio"]}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=find_comments)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-content)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-content)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=find%20comments)**

#### database\_api.find\_comments[](#database_api.find_comments)

Search for comments by author/permlink.

##### Query Parameters JSON[](#database_api.find_comments-parameter_json)

    {"comments": [["author", "permlink"]]}
    

##### Expected Response JSON[](#database_api.find_comments-expected_response_json)

    {"comments": []}
    

##### Example `curl`[](#database_api.find_comments-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.find_comments", "params": {"comments":[["hiveio", "around-the-hive-reflections"]]}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.find_comments", "params": {"comments":[["alice", "a-post-by-alice"]]}, "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF14**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=find_decline_voting_rights_requests)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=find%20decline%20voting%20rights%20requests)**

#### database\_api.find\_decline\_voting\_rights\_requests[](#database_api.find_decline_voting_rights_requests)

Returns a list of requests to decline voting rights.

##### Query Parameters JSON[](#database_api.find_decline_voting_rights_requests-parameter_json)

    {"accounts": []}
    

##### Expected Response JSON[](#database_api.find_decline_voting_rights_requests-expected_response_json)

    {"requests": []}
    

##### Example `curl`[](#database_api.find_decline_voting_rights_requests-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.find_decline_voting_rights_requests", "params": {"accounts":["temp","null"]}, "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF14**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=find_escrows)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-escrow)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-escrow)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=find%20escrows)**

#### database\_api.find\_escrows[](#database_api.find_escrows)

Returns a list of escrows.

##### Query Parameters JSON[](#database_api.find_escrows-parameter_json)

    {"from": ""}
    

##### Expected Response JSON[](#database_api.find_escrows-expected_response_json)

    {
      "escrows": [
        {
          "id": 143,
          "escrow_id": 12345,
          "from": "temp",
          "to": "guest123",
          "agent": "smitop",
          "ratification_deadline": "2038-01-19T03:14:06",
          "escrow_expiration": "2038-01-19T03:14:07",
          "hbd_balance": {
            "amount": "0",
            "precision": 3,
            "nai": "@@000000013"
          },
          "hive_balance": {
            "amount": "1",
            "precision": 3,
            "nai": "@@000000021"
          },
          "pending_fee": {
            "amount": "1",
            "precision": 3,
            "nai": "@@000000021"
          },
          "to_approved": false,
          "agent_approved": false,
          "disputed": false
        }
      ]
    }
    

##### Example `curl`[](#database_api.find_escrows-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.find_escrows", "params": {"from": "temp"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=find_limit_orders)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=find%20limit%20orders)**

#### database\_api.find\_limit\_orders[](#database_api.find_limit_orders)

Returns a list of limit orders.

##### Query Parameters JSON[](#database_api.find_limit_orders-parameter_json)

    {"account": ""}
    

##### Expected Response JSON[](#database_api.find_limit_orders-expected_response_json)

    {
      "orders": [
        {
          "id": 0,
          "created": "2019-12-14T04:05:39",
          "expiration": "2019-12-15T05:05:21",
          "seller": "",
          "orderid": 0,
          "for_sale": 0,
          "sell_price": {
            "base": {
              "amount": "0",
              "precision": 3,
              "nai": "@@000000013"
            },
            "quote": {
              "amount": "0",
              "precision": 3,
              "nai": "@@000000021"
            }
          }
        }
      ]
    }
    

##### Example `curl`[](#database_api.find_limit_orders-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.find_limit_orders", "params": {"account":"temp"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=find_owner_histories)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-owner-history)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-owner-history)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=find%20owner%20histories)**

#### database\_api.find\_owner\_histories[](#database_api.find_owner_histories)

Returns owner authority history. Parameters: `owner:string`

`owner` (string)

 

`"hiveio"`

Queries the owner history for account named “hiveio”.

`"alice"`

Queries the owner history for account named “alice”.

##### Query Parameters JSON[](#database_api.find_owner_histories-parameter_json)

    {"owner": ""}
    

##### Expected Response JSON[](#database_api.find_owner_histories-expected_response_json)

    {"owner_auths": []}
    

##### Example `curl`[](#database_api.find_owner_histories-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.find_owner_histories", "params": {"owner":"hiveio"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.find_owner_histories", "params": {"owner":"alice"}, "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF14**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=find_savings_withdrawals)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-savings-withdraw-from)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-savings-withdraw-from)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=find%20savings%20withdrawals)**

#### database\_api.find\_savings\_withdrawals[](#database_api.find_savings_withdrawals)

Returns the list of savings withdrawls for an account. Parameters: `account:string`

`account` (string)

 

`"hiveio"`

Queries the savings withdraw for account named “hiveio”.

##### Query Parameters JSON[](#database_api.find_savings_withdrawals-parameter_json)

    {"start": null, "limit": 0, "order": "by_name"}
    

##### Expected Response JSON[](#database_api.find_savings_withdrawals-expected_response_json)

    {"withdrawals": []}
    

##### Example `curl`[](#database_api.find_savings_withdrawals-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.find_savings_withdrawals", "params": {"start":"temp"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=find_hbd_conversion_requests)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=find%20hbd%20conversion%20requests)**

#### database\_api.find\_hbd\_conversion\_requests[](#database_api.find_hbd_conversion_requests)

Returns the list of HBD conversion requests for an account. Parameters: `account:string`

`account` (string)

 

`"hiveio"`

Queries a conversion request for hiveio.

`"alice"`

Queries a conversion request for alice.

##### Query Parameters JSON[](#database_api.find_hbd_conversion_requests-parameter_json)

    {"account": ""}
    

##### Expected Response JSON[](#database_api.find_hbd_conversion_requests-expected_response_json)

    {"requests": []}
    

##### Example `curl`[](#database_api.find_hbd_conversion_requests-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.find_hbd_conversion_requests", "params": {"account":"hiveio"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.find_hbd_conversion_requests", "params": {"account":"alice"}, "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF17**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=find_vesting_delegation_expirations)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-vesting-delegations)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.account.html#beem.account.Account.get_expiring_vesting_delegations)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/delegations)
    
*   **[Related](/search/?q=find%20vesting%20delegation%20expirations)**

#### database\_api.find\_vesting\_delegation\_expirations[](#database_api.find_vesting_delegation_expirations)

Returns the expiring vesting delegations for an account. Parameters: `account:string`

`account` (string)

 

 

`"hiveio"`

 

Queries for expiring vesting for `hiveio`.

`"alice"`

 

Queries for expiring vesting for `alice`.

##### Query Parameters JSON[](#database_api.find_vesting_delegation_expirations-parameter_json)

    {"account": ""}
    

##### Expected Response JSON[](#database_api.find_vesting_delegation_expirations-expected_response_json)

    {
      "delegations": [
        {
          "id": 3077902,
          "delegator": "hiveio",
          "vesting_shares": {
            "amount": "201417615",
            "precision": 6,
            "nai": "@@000000037"
          },
          "expiration": "2018-12-05T21:46:48"
        }
      ]
    }
    

##### Example `curl`[](#database_api.find_vesting_delegation_expirations-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.find_vesting_delegation_expirations", "params": {"account":"hiveio"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.find_vesting_delegation_expirations", "params": {"account":"alice"}, "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF17**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=find_vesting_delegations)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-vesting-delegations)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.account.html#beem.account.Account.get_vesting_delegations)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/delegations)
    
*   **[Related](/search/?q=find%20vesting%20delegations)**

#### database\_api.find\_vesting\_delegations[](#database_api.find_vesting_delegations)

Returns the list of vesting delegations for an account. Parameters: `account:string`

`account` (string)

 

 

`"hiveio"`

 

Queries for vesting for `hiveio`.

`"alice"`

 

Queries for vesting for `alice`.

##### Query Parameters JSON[](#database_api.find_vesting_delegations-parameter_json)

    {"account": ""}
    

##### Expected Response JSON[](#database_api.find_vesting_delegations-expected_response_json)

    {
      "delegations": [
        {
          "id": 0,
          "delegator": "",
          "delegatee": "",
          "vesting_shares": {
            "amount": "0",
            "precision": 6,
            "nai": "@@000000037"
          },
          "min_delegation_time": "2018-02-28T15:36:51"
        }
      ]
    }
    

##### Example `curl`[](#database_api.find_vesting_delegations-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.find_vesting_delegations", "params": {"account":"hiveio"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.find_vesting_delegations", "params": {"account":"alice"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=find_votes)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-account-votes)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.account.html#beem.account.Account.get_account_votes)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=find%20votes)**

#### database\_api.find\_votes[](#database_api.find_votes)

Returns all votes for the given post. Required (non-empty) parameters: `author:string`; `permlink:string`

`author` (string)

`permlink` (string)

 

`"hiveio"`

`"announcing-the-launch-of-hive-blockchain"`

Queries votes for content with a slug `@hiveio/announcing-the-launch-of-hive-blockchain`

`"alice"`

`"a-post-by-alice"`

Queries votes for content with a slug `@alice/a-post-by-alice`

##### Query Parameters JSON[](#database_api.find_votes-parameter_json)

    {
      "author": "hiveio",
      "permlink": "announcing-the-launch-of-hive-blockchain"
    }
    

##### Expected Response JSON[](#database_api.find_votes-expected_response_json)

    {
      "votes": [
        {
          "id": 0,
          "voter": "",
          "author": "",
          "permlink": "",
          "weight": "0",
          "rshares": 0,
          "vote_percent": 0,
          "last_update": "2016-04-07T19:15:36",
          "num_changes": -1
        }
      ]
    }
    

##### Example `curl`[](#database_api.find_votes-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.find_votes", "params": {"author":"hiveio", "permlink":"announcing-the-launch-of-hive-blockchain"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.find_votes", "params": {"author":"alice", "permlink":"a-post-by-alice"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=find_withdraw_vesting_routes)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-withdraw-routes)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.account.html#beem.account.Account.get_withdraw_routes)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=find%20withdraw%20vesting%20routes)**

#### database\_api.find\_withdraw\_vesting\_routes[](#database_api.find_withdraw_vesting_routes)

Returns the list of vesting withdraw routes for an account.

##### Query Parameters JSON[](#database_api.find_withdraw_vesting_routes-parameter_json)

    {"account": "", "order": "by_name"}
    

##### Expected Response JSON[](#database_api.find_withdraw_vesting_routes-expected_response_json)

    {
      "routes": [
        {
          "id": 0,
          "from_account": "",
          "to_account": "",
          "percent": 0,
          "auto_vest": true
        }
      ]
    }
    

##### Example `curl`[](#database_api.find_withdraw_vesting_routes-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.find_withdraw_vesting_routes", "params": {"account":"temp", "order":"by_destination"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=find_witnesses)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-witnesses)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-active-witnesses)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/witnesses)
    
*   **[Related](/search/?q=find%20witnesses)**

#### database\_api.find\_witnesses[](#database_api.find_witnesses)

Search for witnesses.

##### Query Parameters JSON[](#database_api.find_witnesses-parameter_json)

    {"owners": []}
    

##### Expected Response JSON[](#database_api.find_witnesses-expected_response_json)

    {
      "witnesses": [
        {
          "id": 0,
          "owner": "initminer",
          "created": "1970-01-01T00:00:00",
          "url": "",
          "votes": 0,
          "virtual_last_update": "225400650183277777230188182",
          "virtual_position": "28933178228158941342755574680549120",
          "virtual_scheduled_time": "340253433742935705172215129634317850517",
          "total_missed": 88,
          "last_aslot": 1202,
          "last_confirmed_block_num": 1092,
          "pow_worker": 0,
          "signing_key": "STM8GC13uCZbP44HzMLV6zPZGwVQ8Nt4Kji8PapsPiNq1BK153XTX",
          "props": {
            "account_creation_fee": {
              "amount": "1",
              "precision": 3,
              "nai": "@@000000021"
            },
            "maximum_block_size": 131072,
            "hbd_interest_rate": 1000,
            "account_subsidy_budget": 797,
            "account_subsidy_decay": 347321
          },
          "hbd_exchange_rate": {
            "base": {
              "amount": "0",
              "precision": 3,
              "nai": "@@000000021"
            },
            "quote": {
              "amount": "0",
              "precision": 3,
              "nai": "@@000000021"
            }
          },
          "last_hbd_exchange_update": "1970-01-01T00:00:00",
          "last_work": "0000000000000000000000000000000000000000000000000000000000000000",
          "running_version": "0.23.0",
          "hardfork_version_vote": "0.23.0",
          "hardfork_time_vote": "2019-10-14T15:00:00",
          "available_witness_account_subsidies": 9379874
        }
      ]
    }
    

##### Example `curl`[](#database_api.find_witnesses-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.find_witnesses", "params": {"owners":["initminer"]}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_active_witnesses)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-active-witnesses)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-active-witnesses)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/witnesses)
    
*   **[Related](/search/?q=get%20active%20witnesses)**

#### database\_api.get\_active\_witnesses[](#database_api.get_active_witnesses)

Returns the list of active witnesses.

##### Query Parameters JSON[](#database_api.get_active_witnesses-parameter_json)

    {}
    

##### Expected Response JSON[](#database_api.get_active_witnesses-expected_response_json)

    {
      "witnesses": [
        "lukestokes.mhth",
        "gtg",
        "ausbitbank",
        "clayop",
        "yabapmatt",
        "curie",
        "thecryptodrive",
        "roelandp",
        "followbtcnews",
        "timcliff",
        "smooth.witness",
        "bhuz",
        "aggroed",
        "blocktrades",
        "cervantes",
        "utopian-io",
        "anyx",
        "jesta",
        "drakos",
        "someguy123",
        "good-karma"
      ]
    }
    

##### Example `curl`[](#database_api.get_active_witnesses-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.get_active_witnesses", "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_config)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-config)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-config)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20config)**

#### database\_api.get\_config[](#database_api.get_config)

Returns information about compile-time constants. Some properties may not be present. See: [Understanding Configuration Values](/tutorials-recipes/understanding-configuration-values.html)

##### Query Parameters JSON[](#database_api.get_config-parameter_json)

    {}
    

##### Expected Response JSON[](#database_api.get_config-expected_response_json)

    {
      "IS_TEST_NET": true,
      "TESTNET_BLOCK_LIMIT": 3000000,
      "SMT_MAX_VOTABLE_ASSETS": 2,
      "SMT_VESTING_WITHDRAW_INTERVAL_SECONDS": 604800,
      "SMT_UPVOTE_LOCKOUT": 43200,
      "SMT_EMISSION_MIN_INTERVAL_SECONDS": 21600,
      "SMT_EMIT_INDEFINITELY": 4294967295,
      "SMT_MAX_NOMINAL_VOTES_PER_DAY": 1000,
      "SMT_MAX_VOTES_PER_REGENERATION": 7000,
      "SMT_DEFAULT_VOTES_PER_REGEN_PERIOD": 50,
      "SMT_DEFAULT_PERCENT_CURATION_REWARDS": 2500,
      "SMT_INITIAL_VESTING_PER_UNIT": 1000000,
      "SMT_BALLAST_SUPPLY_PERCENT": 10,
      "SMT_MAX_ICO_TIERS": 10,
      "HBD_SYMBOL": {"nai": "@@000000013", "precision": 3},
      "HIVE_INITIAL_VOTE_POWER_RATE": 40,
      "HIVE_REDUCED_VOTE_POWER_RATE": 10,
      "HIVE_100_PERCENT": 10000,
      "HIVE_1_PERCENT": 100,
      "HIVE_ACCOUNT_RECOVERY_REQUEST_EXPIRATION_PERIOD": 12000000,
      "HIVE_ACTIVE_CHALLENGE_COOLDOWN": "86400000000",
      "HIVE_ACTIVE_CHALLENGE_FEE": {
        "amount": "2000",
        "precision": 3,
        "nai": "@@000000021"
      },
      "HIVE_ADDRESS_PREFIX": "TST",
      "HIVE_APR_PERCENT_MULTIPLY_PER_BLOCK": "102035135585887",
      "HIVE_APR_PERCENT_MULTIPLY_PER_HOUR": "119577151364285",
      "HIVE_APR_PERCENT_MULTIPLY_PER_ROUND": "133921203762304",
      "HIVE_APR_PERCENT_SHIFT_PER_BLOCK": 87,
      "HIVE_APR_PERCENT_SHIFT_PER_HOUR": 77,
      "HIVE_APR_PERCENT_SHIFT_PER_ROUND": 83,
      "HIVE_BANDWIDTH_AVERAGE_WINDOW_SECONDS": 604800,
      "HIVE_BANDWIDTH_PRECISION": 1000000,
      "HIVE_BENEFICIARY_LIMIT": 128,
      "HIVE_BLOCKCHAIN_PRECISION": 1000,
      "HIVE_BLOCKCHAIN_PRECISION_DIGITS": 3,
      "HIVE_BLOCKCHAIN_HARDFORK_VERSION": "0.23.0",
      "HIVE_BLOCKCHAIN_VERSION": "0.23.0",
      "HIVE_BLOCK_INTERVAL": 3,
      "HIVE_BLOCKS_PER_DAY": 28800,
      "HIVE_BLOCKS_PER_HOUR": 1200,
      "HIVE_BLOCKS_PER_YEAR": 10512000,
      "HIVE_CASHOUT_WINDOW_SECONDS": 3600,
      "HIVE_CASHOUT_WINDOW_SECONDS_PRE_HF12": 3600,
      "HIVE_CASHOUT_WINDOW_SECONDS_PRE_HF17": 3600,
      "HIVE_CHAIN_ID": "18dcf0a285365fc58b71f18b3d3fec954aa0c141c44e4e5cb4cf777b9eab274e",
      "HIVE_COMMENT_REWARD_FUND_NAME": "comment",
      "HIVE_COMMENT_TITLE_LIMIT": 256,
      "HIVE_CONTENT_APR_PERCENT": 3875,
      "HIVE_CONTENT_CONSTANT_HF0": "2000000000000",
      "HIVE_CONTENT_CONSTANT_HF21": "2000000000000",
      "HIVE_CONTENT_REWARD_PERCENT_HF16": 7500,
      "HIVE_CONTENT_REWARD_PERCENT_HF21": 6500,
      "HIVE_CONVERSION_DELAY": "302400000000",
      "HIVE_CONVERSION_DELAY_PRE_HF_16": "604800000000",
      "HIVE_CREATE_ACCOUNT_DELEGATION_RATIO": 5,
      "HIVE_CREATE_ACCOUNT_DELEGATION_TIME": "2592000000000",
      "HIVE_CREATE_ACCOUNT_WITH_HIVE_MODIFIER": 30,
      "HIVE_CURATE_APR_PERCENT": 3875,
      "HIVE_CUSTOM_OP_DATA_MAX_LENGTH": 8192,
      "HIVE_CUSTOM_OP_ID_MAX_LENGTH": 32,
      "HIVE_DEFAULT_HBD_INTEREST_RATE": 1000,
      "HIVE_DOWNVOTE_POOL_PERCENT_HF21": 2500,
      "HIVE_EQUIHASH_K": 6,
      "HIVE_EQUIHASH_N": 140,
      "HIVE_FEED_HISTORY_WINDOW": 84,
      "HIVE_FEED_HISTORY_WINDOW_PRE_HF_16": 168,
      "HIVE_FEED_INTERVAL_BLOCKS": 1200,
      "HIVE_GENESIS_TIME": "2016-01-01T00:00:00",
      "HIVE_HARDFORK_REQUIRED_WITNESSES": 17,
      "HIVE_HF21_CONVERGENT_LINEAR_RECENT_CLAIMS": "503600561838938636",
      "HIVE_INFLATION_NARROWING_PERIOD": 250000,
      "HIVE_INFLATION_RATE_START_PERCENT": 978,
      "HIVE_INFLATION_RATE_STOP_PERCENT": 95,
      "HIVE_INIT_MINER_NAME": "initminer",
      "HIVE_INIT_PUBLIC_KEY_STR": "TST6LLegbAgLAy28EHrffBVuANFWcFgmqRMW13wBmTExqFE9SCkg4",
      "HIVE_INIT_SUPPLY": "250000000000",
      "HIVE_HBD_INIT_SUPPLY": "7000000000",
      "HIVE_INIT_TIME": "1970-01-01T00:00:00",
      "HIVE_IRREVERSIBLE_THRESHOLD": 7500,
      "HIVE_LIQUIDITY_APR_PERCENT": 750,
      "HIVE_LIQUIDITY_REWARD_BLOCKS": 1200,
      "HIVE_LIQUIDITY_REWARD_PERIOD_SEC": 3600,
      "HIVE_LIQUIDITY_TIMEOUT_SEC": "604800000000",
      "HIVE_MAX_ACCOUNT_CREATION_FEE": 1000000000,
      "HIVE_MAX_ACCOUNT_NAME_LENGTH": 16,
      "HIVE_MAX_ACCOUNT_WITNESS_VOTES": 30,
      "HIVE_MAX_ASSET_WHITELIST_AUTHORITIES": 10,
      "HIVE_MAX_AUTHORITY_MEMBERSHIP": 40,
      "HIVE_MAX_BLOCK_SIZE": 393216000,
      "HIVE_SOFT_MAX_BLOCK_SIZE": 2097152,
      "HIVE_MAX_CASHOUT_WINDOW_SECONDS": 86400,
      "HIVE_MAX_COMMENT_DEPTH": 65535,
      "HIVE_MAX_COMMENT_DEPTH_PRE_HF17": 6,
      "HIVE_MAX_FEED_AGE_SECONDS": 604800,
      "HIVE_MAX_INSTANCE_ID": "281474976710655",
      "HIVE_MAX_MEMO_SIZE": 2048,
      "HIVE_MAX_WITNESSES": 21,
      "HIVE_MAX_MINER_WITNESSES_HF0": 1,
      "HIVE_MAX_MINER_WITNESSES_HF17": 0,
      "HIVE_MAX_PERMLINK_LENGTH": 256,
      "HIVE_MAX_PROXY_RECURSION_DEPTH": 4,
      "HIVE_MAX_RATION_DECAY_RATE": 1000000,
      "HIVE_MAX_RESERVE_RATIO": 20000,
      "HIVE_MAX_RUNNER_WITNESSES_HF0": 1,
      "HIVE_MAX_RUNNER_WITNESSES_HF17": 1,
      "HIVE_MAX_SATOSHIS": "4611686018427387903",
      "HIVE_MAX_SHARE_SUPPLY": "1000000000000000",
      "HIVE_MAX_SIG_CHECK_DEPTH": 2,
      "HIVE_MAX_SIG_CHECK_ACCOUNTS": 125,
      "HIVE_MAX_TIME_UNTIL_EXPIRATION": 3600,
      "HIVE_MAX_TRANSACTION_SIZE": 65536,
      "HIVE_MAX_UNDO_HISTORY": 10000,
      "HIVE_MAX_URL_LENGTH": 127,
      "HIVE_MAX_VOTE_CHANGES": 5,
      "HIVE_MAX_VOTED_WITNESSES_HF0": 19,
      "HIVE_MAX_VOTED_WITNESSES_HF17": 20,
      "HIVE_MAX_WITHDRAW_ROUTES": 10,
      "HIVE_MAX_WITNESS_URL_LENGTH": 2048,
      "HIVE_MIN_ACCOUNT_CREATION_FEE": 0,
      "HIVE_MIN_ACCOUNT_NAME_LENGTH": 3,
      "HIVE_MIN_BLOCK_SIZE_LIMIT": 65536,
      "HIVE_MIN_BLOCK_SIZE": 115,
      "HIVE_MIN_CONTENT_REWARD": {
        "amount": "1000",
        "precision": 3,
        "nai": "@@000000021"
      },
      "HIVE_MIN_CURATE_REWARD": {
        "amount": "1000",
        "precision": 3,
        "nai": "@@000000021"
      },
      "HIVE_MIN_PERMLINK_LENGTH": 0,
      "HIVE_MIN_REPLY_INTERVAL": 20000000,
      "HIVE_MIN_REPLY_INTERVAL_HF20": 3000000,
      "HIVE_MIN_ROOT_COMMENT_INTERVAL": 300000000,
      "HIVE_MIN_COMMENT_EDIT_INTERVAL": 3000000,
      "HIVE_MIN_VOTE_INTERVAL_SEC": 3,
      "HIVE_MINER_ACCOUNT": "miners",
      "HIVE_MINER_PAY_PERCENT": 100,
      "HIVE_MIN_FEEDS": 7,
      "HIVE_MINING_REWARD": {
        "amount": "1000",
        "precision": 3,
        "nai": "@@000000021"
      },
      "HIVE_MINING_TIME": "2016-01-01T00:00:00",
      "HIVE_MIN_LIQUIDITY_REWARD": {
        "amount": "1200000",
        "precision": 3,
        "nai": "@@000000021"
      },
      "HIVE_MIN_LIQUIDITY_REWARD_PERIOD_SEC": 60000000,
      "HIVE_MIN_PAYOUT_HBD": {
        "amount": "20",
        "precision": 3,
        "nai": "@@000000013"
      },
      "HIVE_MIN_POW_REWARD": {
        "amount": "1000",
        "precision": 3,
        "nai": "@@000000021"
      },
      "HIVE_MIN_PRODUCER_REWARD": {
        "amount": "1000",
        "precision": 3,
        "nai": "@@000000021"
      },
      "HIVE_MIN_TRANSACTION_EXPIRATION_LIMIT": 15,
      "HIVE_MIN_TRANSACTION_SIZE_LIMIT": 1024,
      "HIVE_MIN_UNDO_HISTORY": 10,
      "HIVE_NULL_ACCOUNT": "null",
      "HIVE_NUM_INIT_MINERS": 1,
      "HIVE_OWNER_AUTH_HISTORY_TRACKING_START_BLOCK_NUM": 1,
      "HIVE_OWNER_AUTH_RECOVERY_PERIOD": 60000000,
      "HIVE_OWNER_CHALLENGE_COOLDOWN": "86400000000",
      "HIVE_OWNER_CHALLENGE_FEE": {
        "amount": "30000",
        "precision": 3,
        "nai": "@@000000021"
      },
      "HIVE_OWNER_UPDATE_LIMIT": 0,
      "HIVE_POST_AVERAGE_WINDOW": 86400,
      "HIVE_POST_REWARD_FUND_NAME": "post",
      "HIVE_POST_WEIGHT_CONSTANT": 1600000000,
      "HIVE_POW_APR_PERCENT": 750,
      "HIVE_PRODUCER_APR_PERCENT": 750,
      "HIVE_PROXY_TO_SELF_ACCOUNT": "",
      "HIVE_HBD_INTEREST_COMPOUND_INTERVAL_SEC": 2592000,
      "HIVE_SECONDS_PER_YEAR": 31536000,
      "HIVE_PROPOSAL_FUND_PERCENT_HF0": 0,
      "HIVE_PROPOSAL_FUND_PERCENT_HF21": 1000,
      "HIVE_RECENT_RSHARES_DECAY_TIME_HF19": "1296000000000",
      "HIVE_RECENT_RSHARES_DECAY_TIME_HF17": "2592000000000",
      "HIVE_REVERSE_AUCTION_WINDOW_SECONDS_HF6": 1800,
      "HIVE_REVERSE_AUCTION_WINDOW_SECONDS_HF20": 900,
      "HIVE_REVERSE_AUCTION_WINDOW_SECONDS_HF21": 300,
      "HIVE_ROOT_POST_PARENT": "",
      "HIVE_SAVINGS_WITHDRAW_REQUEST_LIMIT": 100,
      "HIVE_SAVINGS_WITHDRAW_TIME": "259200000000",
      "HIVE_HBD_START_PERCENT_HF14": 200,
      "HIVE_HBD_START_PERCENT_HF20": 900,
      "HIVE_HBD_STOP_PERCENT_HF14": 500,
      "HIVE_HBD_STOP_PERCENT_HF20": 1000,
      "HIVE_SECOND_CASHOUT_WINDOW": 259200,
      "HIVE_SOFT_MAX_COMMENT_DEPTH": 255,
      "HIVE_START_MINER_VOTING_BLOCK": 864000,
      "HIVE_START_VESTING_BLOCK": 201600,
      "HIVE_TEMP_ACCOUNT": "temp",
      "HIVE_UPVOTE_LOCKOUT_HF7": 60000000,
      "HIVE_UPVOTE_LOCKOUT_HF17": 300000000,
      "HIVE_UPVOTE_LOCKOUT_SECONDS": 300,
      "HIVE_VESTING_FUND_PERCENT_HF16": 1500,
      "HIVE_VESTING_WITHDRAW_INTERVALS": 13,
      "HIVE_VESTING_WITHDRAW_INTERVALS_PRE_HF_16": 104,
      "HIVE_VESTING_WITHDRAW_INTERVAL_SECONDS": 604800,
      "HIVE_VOTE_DUST_THRESHOLD": 50000000,
      "HIVE_VOTING_MANA_REGENERATION_SECONDS": 432000,
      "HIVE_SYMBOL": {"nai": "@@000000021", "precision": 3},
      "VESTS_SYMBOL": {"nai": "@@000000037", "precision": 6},
      "HIVE_VIRTUAL_SCHEDULE_LAP_LENGTH": "18446744073709551615",
      "HIVE_VIRTUAL_SCHEDULE_LAP_LENGTH2": "340282366920938463463374607431768211455",
      "HIVE_VOTES_PER_PERIOD_SMT_HF": 50,
      "HIVE_MAX_LIMIT_ORDER_EXPIRATION": 2419200,
      "HIVE_DELEGATION_RETURN_PERIOD_HF0": 3600,
      "HIVE_DELEGATION_RETURN_PERIOD_HF20": 432000,
      "HIVE_RD_MIN_DECAY_BITS": 6,
      "HIVE_RD_MAX_DECAY_BITS": 32,
      "HIVE_RD_DECAY_DENOM_SHIFT": 36,
      "HIVE_RD_MAX_POOL_BITS": 64,
      "HIVE_RD_MAX_BUDGET_1": "17179869183",
      "HIVE_RD_MAX_BUDGET_2": 268435455,
      "HIVE_RD_MAX_BUDGET_3": 2147483647,
      "HIVE_RD_MAX_BUDGET": 268435455,
      "HIVE_RD_MIN_DECAY": 64,
      "HIVE_RD_MIN_BUDGET": 1,
      "HIVE_RD_MAX_DECAY": 4294967295,
      "HIVE_ACCOUNT_SUBSIDY_PRECISION": 10000,
      "HIVE_WITNESS_SUBSIDY_BUDGET_PERCENT": 12500,
      "HIVE_WITNESS_SUBSIDY_DECAY_PERCENT": 210000,
      "HIVE_DEFAULT_ACCOUNT_SUBSIDY_DECAY": 347321,
      "HIVE_DEFAULT_ACCOUNT_SUBSIDY_BUDGET": 797,
      "HIVE_DECAY_BACKSTOP_PERCENT": 9000,
      "HIVE_BLOCK_GENERATION_POSTPONED_TX_LIMIT": 5,
      "HIVE_PENDING_TRANSACTION_EXECUTION_LIMIT": 200000,
      "HIVE_TREASURY_ACCOUNT": "hive.fund",
      "HIVE_TREASURY_FEE": 10000,
      "HIVE_PROPOSAL_MAINTENANCE_PERIOD": 3600,
      "HIVE_PROPOSAL_MAINTENANCE_CLEANUP": 86400,
      "HIVE_PROPOSAL_SUBJECT_MAX_LENGTH": 80,
      "HIVE_PROPOSAL_MAX_IDS_NUMBER": 5,
      "HIVE_NETWORK_TYPE": "testnet",
      "HIVE_DB_FORMAT_VERSION": "1"
    }
    

##### Example `curl`[](#database_api.get_config-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.get_config", "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_current_price_feed)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-current-median-history-price)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.blockchaininstance.html#beem.blockchaininstance.BlockChainInstance.get_median_price)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20current%20price%20feed)**

#### database\_api.get\_current\_price\_feed[](#database_api.get_current_price_feed)

Returns the current price feed.

##### Query Parameters JSON[](#database_api.get_current_price_feed-parameter_json)

    {}
    

##### Expected Response JSON[](#database_api.get_current_price_feed-expected_response_json)

    {
      "base": {
        "amount": "1",
        "precision": 3,
        "nai": "@@000000013"
      },
      "quote": {
        "amount": "1",
        "precision": 3,
        "nai": "@@000000021"
      }
    }
    

##### Example `curl`[](#database_api.get_current_price_feed-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.get_current_price_feed", "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_dynamic_global_properties)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-dynamic-global-properties)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.blockchaininstance.html#beem.blockchaininstance.BlockChainInstance.get_dynamic_global_properties)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/dynamicglobalproperties)
    
*   **[Related](/search/?q=get%20dynamic%20global%20properties)**

#### database\_api.get\_dynamic\_global\_properties[](#database_api.get_dynamic_global_properties)

Returns the current dynamic global properties. See: [Understanding Dynamic Global Properties](/tutorials-recipes/understanding-dynamic-global-properties.html)

##### Query Parameters JSON[](#database_api.get_dynamic_global_properties-parameter_json)

    {}
    

##### Expected Response JSON[](#database_api.get_dynamic_global_properties-expected_response_json)

    {
      "id": 0,
      "head_block_number": 293261,
      "head_block_id": "0004798df7357f23b9e6d4b6739e4ca9eac2f403",
      "time": "2019-12-14T22:58:51",
      "current_witness": "init-0",
      "total_pow": "18446744073709551615",
      "num_pow_witnesses": 0,
      "virtual_supply": {
        "amount": "286041551516",
        "precision": 3,
        "nai": "@@000000021"
      },
      "current_supply": {
        "amount": "250990841260",
        "precision": 3,
        "nai": "@@000000021"
      },
      "confidential_supply": {
        "amount": "0",
        "precision": 3,
        "nai": "@@000000021"
      },
      "init_hbd_supply": {
        "amount": "7000000000",
        "precision": 3,
        "nai": "@@000000013"
      },
      "current_hbd_supply": {
        "amount": "35050710256",
        "precision": 3,
        "nai": "@@000000013"
      },
      "confidential_hbd_supply": {
        "amount": "0",
        "precision": 3,
        "nai": "@@000000013"
      },
      "total_vesting_fund_hive": {
        "amount": "146016220388",
        "precision": 3,
        "nai": "@@000000021"
      },
      "total_vesting_shares": {
        "amount": "52556676118700",
        "precision": 6,
        "nai": "@@000000037"
      },
      "total_reward_fund_hive": {
        "amount": "0",
        "precision": 3,
        "nai": "@@000000021"
      },
      "total_reward_shares2": "0",
      "pending_rewarded_vesting_shares": {
        "amount": "55809356614",
        "precision": 6,
        "nai": "@@000000037"
      },
      "pending_rewarded_vesting_hive": {
        "amount": "154999023",
        "precision": 3,
        "nai": "@@000000021"
      },
      "hbd_interest_rate": 1000,
      "hbd_print_rate": 0,
      "maximum_block_size": 131072,
      "required_actions_partition_percent": 2500,
      "current_aslot": 41585977,
      "recent_slots_filled": "340282366920938463463374607431768211455",
      "participation_count": 128,
      "last_irreversible_block_num": 293240,
      "target_votes_per_period": 50,
      "delegation_return_period": 432000,
      "reverse_auction_seconds": 300,
      "available_account_subsidies": 120334411,
      "hbd_stop_percent": 1000,
      "hbd_start_percent": 900,
      "next_maintenance_time": "2019-12-14T23:18:24",
      "last_budget_time": "2019-12-14T22:18:24",
      "content_reward_percent": 6500,
      "vesting_reward_percent": 1500,
      "sps_fund_percent": 1000,
      "sps_interval_ledger": {
        "amount": "213590",
        "precision": 3,
        "nai": "@@000000013"
      },
      "downvote_pool_percent": 2500,
      "smt_creation_fee": {
        "amount": "1000",
        "precision": 3,
        "nai": "@@000000013"
      }
    }
    

##### Example `curl`[](#database_api.get_dynamic_global_properties-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.get_dynamic_global_properties", "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_feed_history)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-current-median-history-price)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.blockchaininstance.html#beem.blockchaininstance.BlockChainInstance.get_median_price)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20feed%20history)**

#### database\_api.get\_feed\_history[](#database_api.get_feed_history)

Returns the history of price feed values.

##### Query Parameters JSON[](#database_api.get_feed_history-parameter_json)

    {}
    

##### Expected Response JSON[](#database_api.get_feed_history-expected_response_json)

    {
      "id": 0,
      "current_median_history": {
        "base": {
          "amount": "1",
          "precision": 3,
          "nai": "@@000000013"
        },
        "quote": {
          "amount": "1",
          "precision": 3,
          "nai": "@@000000021"
        }
      },
      "price_history": []
    }
    

##### Example `curl`[](#database_api.get_feed_history-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.get_feed_history", "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_hardfork_properties)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-hardfork-version)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.blockchaininstance.html#beem.blockchaininstance.BlockChainInstance.get_hardfork_properties)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/database-diagram#blocks-and-transactions)
    
*   **[Related](/search/?q=get%20hardfork%20properties)**

#### database\_api.get\_hardfork\_properties[](#database_api.get_hardfork_properties)

Returns the current properties about the blockchain’s hardforks.

See: [condenser\_api.get\_next\_scheduled\_hardfork](/apidefinitions/#condenser_api.get_next_scheduled_hardfork), [hardfork](/apidefinitions/#broadcast_ops_hardfork)

##### Query Parameters JSON[](#database_api.get_hardfork_properties-parameter_json)

    {}
    

##### Expected Response JSON[](#database_api.get_hardfork_properties-expected_response_json)

    {
      "id": 0,
      "processed_hardforks": [
        "2016-03-24T16:00:00",
        "2016-04-25T17:30:00",
        "2016-04-26T18:00:00",
        "2016-04-27T13:00:00",
        "2016-04-30T15:00:00",
        "2016-05-31T17:00:00",
        "2016-06-30T14:00:00",
        "2016-07-04T00:00:00",
        "2016-07-04T01:00:00",
        "2016-07-14T00:00:00",
        "2016-07-15T12:00:00",
        "2016-07-17T15:00:00",
        "2016-07-26T15:00:00",
        "2016-08-15T14:00:00",
        "2016-09-20T15:00:00",
        "2016-11-08T16:00:00",
        "2016-12-06T16:00:00",
        "2017-03-30T15:00:00",
        "2017-03-30T15:00:00",
        "2017-06-20T15:00:00",
        "2018-09-25T15:00:00",
        "2019-08-27T15:00:00",
        "2019-08-29T15:00:00",
        "2020-03-20T14:00:00",
        "2020-10-06T14:00:00",
        "2021-06-30T14:00:00",
        "2022-10-11T12:00:00"
      ],
      "last_hardfork": 26,
      "current_hardfork_version": "1.26.0",
      "next_hardfork": "1.26.0",
      "next_hardfork_time": "2022-10-11T12:00:00"
    }
    

##### Example `curl`[](#database_api.get_hardfork_properties-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.get_hardfork_properties", "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_order_book)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-order-book)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20order%20book)**

#### database\_api.get\_order\_book[](#database_api.get_order_book)

Returns the order book.

##### Query Parameters JSON[](#database_api.get_order_book-parameter_json)

    {
      "limit": 0,
      "base": {
        "amount": "1000",
        "precision": 3,
        "nai": "@@000000021"
      },
      "quote": {
        "amount": "1",
        "precision": 3,
        "nai": "@@000000013"
      }
    }
    

##### Expected Response JSON[](#database_api.get_order_book-expected_response_json)

    {"asks": [], "bids": []}
    

##### Example `curl`[](#database_api.get_order_book-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.get_order_book", "params":{"limit":10,"base":{"amount":"1000","precision":3,"nai":"@@000000021"},"quote":{"amount":"1","precision":3,"nai":"@@000000013"}}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.get_order_book", "params":{"limit":50,"base":{"amount":"1000","precision":3,"nai":"@@000000021"},"quote":{"amount":"1","precision":3,"nai":"@@000000013"}}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-potential-signatures)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-potential-signatures)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20potential%20signatures)**

#### database\_api.get\_potential\_signatures[](#database_api.get_potential_signatures)

This method will return the set of all public keys that could possibly sign for a given transaction. This call can be used by wallets to filter their set of public keys to just the relevant subset prior to calling `get_required_signatures` to get the minimum subset.

##### Query Parameters JSON[](#database_api.get_potential_signatures-parameter_json)

    {
      "trx": {
        "ref_block_num": 0,
        "ref_block_prefix": 0,
        "expiration": "1970-01-01T00:00:00",
        "operations": [],
        "extensions": [],
        "signatures": []
      }
    }
    

##### Expected Response JSON[](#database_api.get_potential_signatures-expected_response_json)

    {"keys": []}
    

##### Example `curl`[](#database_api.get_potential_signatures-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.get_potential_signatures", "params":{"trx":{"ref_block_num":1097,"ref_block_prefix":2181793527,"expiration":"2016-03-24T18:00:21","operations":[{"type":"pow_operation","value":{"worker_account":"cloop3","block_id":"00000449f7860b82b4fbe2f317c670e9f01d6d9a","nonce":3899,"work":{"worker":"STM7P5TDnA87Pj9T4mf6YHrhzjC1KbPZpNxLWCcVcHxNYXakpoT4F","input":"ae8e7c677119d22385f8c48026fee7aad7bba693bf788d7f27047f40b47738c0","signature":"1f38fe9a3f9989f84bd94aa5bbc88beaf09b67f825aa4450cf5105d111149ba6db560b582c7dbb026c7fc9c2eb5051815a72b17f6896ed59d3851d9a0f9883ca7a","work":"000e7b209d58f2e64b36e9bf12b999c6c7af168cc3fc41eb7f8a4bf796c174c3"},"props":{"account_creation_fee":{"amount":"100000","precision":3,"nai":"@@000000021"},"maximum_block_size":131072,"hbd_interest_rate":1000}}}],"extensions":[],"signatures":[]}}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-required-signatures)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-required-signatures)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20required%20signatures)**

#### database\_api.get\_required\_signatures[](#database_api.get_required_signatures)

This API will take a partially signed transaction and a set of public keys that the owner has the ability to sign for and return the minimal subset of public keys that should add signatures to the transaction.

##### Query Parameters JSON[](#database_api.get_required_signatures-parameter_json)

    {
      "trx": {
        "ref_block_num": 0,
        "ref_block_prefix": 0,
        "expiration": "1970-01-01T00:00:00",
        "operations": [],
        "extensions": [],
        "signatures": []
      },
      "available_keys": []
    }
    

##### Expected Response JSON[](#database_api.get_required_signatures-expected_response_json)

    {"keys": []}
    

##### Example `curl`[](#database_api.get_required_signatures-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.get_required_signatures", "params":{"trx":{"ref_block_num":1097,"ref_block_prefix":2181793527,"expiration":"2016-03-24T18:00:21","operations":[{"type":"pow_operation","value":{"worker_account":"cloop3","block_id":"00000449f7860b82b4fbe2f317c670e9f01d6d9a","nonce":3899,"work":{"worker":"STM7P5TDnA87Pj9T4mf6YHrhzjC1KbPZpNxLWCcVcHxNYXakpoT4F","input":"ae8e7c677119d22385f8c48026fee7aad7bba693bf788d7f27047f40b47738c0","signature":"1f38fe9a3f9989f84bd94aa5bbc88beaf09b67f825aa4450cf5105d111149ba6db560b582c7dbb026c7fc9c2eb5051815a72b17f6896ed59d3851d9a0f9883ca7a","work":"000e7b209d58f2e64b36e9bf12b999c6c7af168cc3fc41eb7f8a4bf796c174c3"},"props":{"account_creation_fee":{"amount":"100000","precision":3,"nai":"@@000000021"},"maximum_block_size":131072,"hbd_interest_rate":1000}}}],"extensions":[],"signatures":[]},"available_keys":[]}, "id ":1}' https://api.hive.blog
    

* * *

*   **Since: HF17**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_reward_funds)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-reward-fund)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-reward-fund)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20reward%20funds)**

#### database\_api.get\_reward\_funds[](#database_api.get_reward_funds)

Returns information about the current reward funds.

##### Query Parameters JSON[](#database_api.get_reward_funds-parameter_json)

    {}
    

##### Expected Response JSON[](#database_api.get_reward_funds-expected_response_json)

    {
      "funds": [
        {
          "id": 0,
          "name": "post",
          "reward_balance": {
            "amount": "189101553",
            "precision": 3,
            "nai": "@@000000021"
          },
          "recent_claims": "2723043883497",
          "last_update": "2019-12-14T23:10:42",
          "content_constant": "2000000000000",
          "percent_curation_rewards": 5000,
          "percent_content_rewards": 10000,
          "author_reward_curve": "convergent_linear",
          "curation_reward_curve": "convergent_square_root"
        }
      ]
    }
    

##### Example `curl`[](#database_api.get_reward_funds-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.get_reward_funds", "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-transaction-hex)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-transaction-hex)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20transaction%20hex)**

#### database\_api.get\_transaction\_hex[](#database_api.get_transaction_hex)

Returns a hexdump of the serialized binary form of a transaction.

##### Query Parameters JSON[](#database_api.get_transaction_hex-parameter_json)

    {
      "trx": {
        "ref_block_num": 0,
        "ref_block_prefix": 0,
        "expiration": "1970-01-01T00:00:00",
        "operations": [],
        "extensions": [],
        "signatures": []
      }
    }
    

##### Expected Response JSON[](#database_api.get_transaction_hex-expected_response_json)

    {"hex": "00000000000000000000000000"}
    

##### Example `curl`[](#database_api.get_transaction_hex-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.get_transaction_hex", "params":{"trx":{"ref_block_num":1097,"ref_block_prefix":2181793527,"expiration":"2016-03-24T18:00:21","operations":[{"type":"pow_operation","value":{"worker_account":"cloop3","block_id":"00000449f7860b82b4fbe2f317c670e9f01d6d9a","nonce":3899,"work":{"worker":"STM7P5TDnA87Pj9T4mf6YHrhzjC1KbPZpNxLWCcVcHxNYXakpoT4F","input":"ae8e7c677119d22385f8c48026fee7aad7bba693bf788d7f27047f40b47738c0","signature":"1f38fe9a3f9989f84bd94aa5bbc88beaf09b67f825aa4450cf5105d111149ba6db560b582c7dbb026c7fc9c2eb5051815a72b17f6896ed59d3851d9a0f9883ca7a","work":"000e7b209d58f2e64b36e9bf12b999c6c7af168cc3fc41eb7f8a4bf796c174c3"},"props":{"account_creation_fee":{"amount":"100000","precision":3,"nai":"@@000000021"},"maximum_block_size":131072,"hbd_interest_rate":1000}}}],"extensions":[],"signatures":[]}}, "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF20**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_version)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-version)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-version)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20version)**

#### database\_api.get\_version[](#database_api.get_version)

Returns the compile time versions of blockchain, hived, FC. Also returns the boot time version of the chain id (_may_ be different from compile time value only when looking at a testnet)

##### Query Parameters JSON[](#database_api.get_version-parameter_json)

    {}
    

##### Expected Response JSON[](#database_api.get_version-expected_response_json)

    {
      "blockchain_version": "0.23.0",
      "hive_revision": "5cda10a488cf77f68549ec6d3a6be9af2ea9351b",
      "fc_revision": "5cda10a488cf77f68549ec6d3a6be9af2ea9351b",
      "chain_id": "beeab0de00000000000000000000000000000000000000000000000000000000"
    }
    

##### Example `curl`[](#database_api.get_version-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.get_version", "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=get_witness_schedule)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-witness-schedule)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-witness-schedule)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/witnesses)
    
*   **[Related](/search/?q=get%20witness%20schedule)**

#### database\_api.get\_witness\_schedule[](#database_api.get_witness_schedule)

Returns the current witness schedule.

##### Query Parameters JSON[](#database_api.get_witness_schedule-parameter_json)

    {}
    

##### Expected Response JSON[](#database_api.get_witness_schedule-expected_response_json)

    {
      "id": 0,
      "current_virtual_time": "55892543567970911424442556665819",
      "next_shuffle_block_num": 293580,
      "current_shuffled_witnesses": [
        "init-2",
        "init-11",
        "init-18",
        "init-16",
        "init-1",
        "init-10",
        "init-0",
        "init-14",
        "init-13",
        "gandalf",
        "init-3",
        "init-12",
        "init-5",
        "init-17",
        "initminer",
        "init-19",
        "init-4",
        "init-15",
        "drakos",
        "gtg",
        "init-7"
      ],
      "num_scheduled_witnesses": 21,
      "elected_weight": 1,
      "timeshare_weight": 5,
      "miner_weight": 1,
      "witness_pay_normalization_factor": 25,
      "median_props": {
        "account_creation_fee": {
          "amount": "0",
          "precision": 3,
          "nai": "@@000000021"
        },
        "maximum_block_size": 131072,
        "hbd_interest_rate": 1000,
        "account_subsidy_budget": 797,
        "account_subsidy_decay": 347321
      },
      "majority_version": "0.23.0",
      "max_voted_witnesses": 20,
      "max_miner_witnesses": 0,
      "max_runner_witnesses": 1,
      "hardfork_required_witnesses": 17,
      "account_subsidy_rd": {
        "resource_unit": 10000,
        "budget_per_time_unit": 797,
        "pool_eq": 157691079,
        "max_pool_size": 157691079,
        "decay_params": {
          "decay_per_time_unit": 347321,
          "decay_per_time_unit_denom_shift": 36
        },
        "min_decay": 0
      },
      "account_subsidy_witness_rd": {
        "resource_unit": 10000,
        "budget_per_time_unit": 996,
        "pool_eq": 9384019,
        "max_pool_size": 9384019,
        "decay_params": {
          "decay_per_time_unit": 7293741,
          "decay_per_time_unit_denom_shift": 36
        },
        "min_decay": 612
      },
      "min_witness_account_subsidy_decay": 0
    }
    

##### Example `curl`[](#database_api.get_witness_schedule-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.get_witness_schedule", "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF11**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=list_account_recovery_requests)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-recovery-request)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-recovery-request)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=list%20account%20recovery%20requests)**

#### database\_api.list\_account\_recovery\_requests[](#database_api.list_account_recovery_requests)

Returns a list of account recovery requests. Parameters: `start:string`, `limit:int`, `order:string`

*   `limit` is up to 1000.
*   `order` can be one of:
    *   `by_account` - order by accont name
    *   `by_expiration` - order by expiration

`account` (string)

`limit` (int)

`order` (string)

 

`"hiveio"`

10

`"by_account"`

Queries the recovery requests for account named “hiveio”, ordered by account name.

`["1960-01-01T00:00:00"]`

10

`"by_expiration"`

Queries the recovery requests for date, ordered by expiration.

##### Query Parameters JSON[](#database_api.list_account_recovery_requests-parameter_json)

    {"start": null, "limit": 0, "order": "by_name"}
    

##### Expected Response JSON[](#database_api.list_account_recovery_requests-expected_response_json)

    {"requests": []}
    

##### Example `curl`[](#database_api.list_account_recovery_requests-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_account_recovery_requests", "params": {"start":"", "limit":10, "order":"by_account"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_account_recovery_requests", "params": {"start":["1960-01-01T00:00:00"], "limit":10, "order":"by_expiration"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=list_accounts)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-accounts)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.blockchain.html#beem.blockchain.Blockchain.get_all_accounts)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=list%20accounts)**

#### database\_api.list\_accounts[](#database_api.list_accounts)

List accounts ordered by specified key. Parameters: `start:object`, `limit:int`, `order:string`, `delayed_votes_active:boolean`

*   `limit` is up to 1000.
*   `order` can be one of:
    *   `by_name` - order by accont name
    *   `by_proxy` - order by proxy
    *   `by_next_vesting_withdrawal` - order by next next vesting withdrawal
*   `delayed_votes_active` default true (optional)

`start` (object)

`limit` (int)

`order` (string)

`delayed_votes_active` (boolean)

`""`

`10`

`"by_name"` Queries for up to 10 accounts starting at the beginning, sorted by name.

 

`["", ""]`

`10`

`"by_proxy"` Queries for up to 10 accounts starting at the beginning, sorted by proxy.

 

`["1960-01-01T00:00:00", ""]`

`10`

`"by_next_vesting_withdrawal"` Queries for up to 10 accounts starting at the beginning, sorted by next vesting withdrawl.

false

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#database_apilist_accounts)

##### Query Parameters JSON[](#database_api.list_accounts-parameter_json)

    {
      "start": null,
      "limit": 0,
      "order": "by_name",
      "delayed_votes_active": true
    }
    

##### Expected Response JSON[](#database_api.list_accounts-expected_response_json)

    {
      "accounts": [
        {
          "id": 7184,
          "name": "a-0",
          "owner": {
            "weight_threshold": 1,
            "account_auths": [],
            "key_auths": [
              [
                "STM5RrTRNDhhrMaA24SzSeE5AvmUcutb1q1VZp1imnT8p871s3UjN",
                1
              ]
            ]
          },
          "active": {
            "weight_threshold": 1,
            "account_auths": [],
            "key_auths": [
              [
                "STM5RrTRNDhhrMaA24SzSeE5AvmUcutb1q1VZp1imnT8p871s3UjN",
                1
              ]
            ]
          },
          "posting": {
            "weight_threshold": 1,
            "account_auths": [],
            "key_auths": [
              [
                "STM5RrTRNDhhrMaA24SzSeE5AvmUcutb1q1VZp1imnT8p871s3UjN",
                1
              ]
            ]
          },
          "memo_key": "STM5RrTRNDhhrMaA24SzSeE5AvmUcutb1q1VZp1imnT8p871s3UjN",
          "json_metadata": "",
          "posting_json_metadata": "",
          "proxy": "",
          "last_owner_update": "1970-01-01T00:00:00",
          "last_account_update": "1970-01-01T00:00:00",
          "created": "2016-04-30T12:27:12",
          "mined": true,
          "recovery_account": "hiveio",
          "last_account_recovery": "1970-01-01T00:00:00",
          "reset_account": "null",
          "comment_count": 0,
          "lifetime_vote_count": 0,
          "post_count": 0,
          "can_vote": true,
          "voting_manabar": {
            "current_mana": 10000,
            "last_update_time": 1462019232
          },
          "downvote_manabar": {
            "current_mana": 0,
            "last_update_time": 1462019232
          },
          "balance": {
            "amount": "1",
            "precision": 3,
            "nai": "@@000000021"
          },
          "savings_balance": {
            "amount": "0",
            "precision": 3,
            "nai": "@@000000021"
          },
          "hbd_balance": {
            "amount": "0",
            "precision": 3,
            "nai": "@@000000013"
          },
          "hbd_seconds": "0",
          "hbd_seconds_last_update": "1970-01-01T00:00:00",
          "hbd_last_interest_payment": "1970-01-01T00:00:00",
          "savings_hbd_balance": {
            "amount": "0",
            "precision": 3,
            "nai": "@@000000013"
          },
          "savings_hbd_seconds": "0",
          "savings_hbd_seconds_last_update": "1970-01-01T00:00:00",
          "savings_hbd_last_interest_payment": "1970-01-01T00:00:00",
          "savings_withdraw_requests": 0,
          "reward_hbd_balance": {
            "amount": "0",
            "precision": 3,
            "nai": "@@000000013"
          },
          "reward_hive_balance": {
            "amount": "0",
            "precision": 3,
            "nai": "@@000000021"
          },
          "reward_vesting_balance": {
            "amount": "0",
            "precision": 6,
            "nai": "@@000000037"
          },
          "reward_vesting_hive": {
            "amount": "0",
            "precision": 3,
            "nai": "@@000000021"
          },
          "vesting_shares": {
            "amount": "13873020360",
            "precision": 6,
            "nai": "@@000000037"
          },
          "delegated_vesting_shares": {
            "amount": "0",
            "precision": 6,
            "nai": "@@000000037"
          },
          "received_vesting_shares": {
            "amount": "0",
            "precision": 6,
            "nai": "@@000000037"
          },
          "vesting_withdraw_rate": {
            "amount": "0",
            "precision": 6,
            "nai": "@@000000037"
          },
          "post_voting_power": {
            "amount": "13873020360",
            "precision": 6,
            "nai": "@@000000037"
          },
          "next_vesting_withdrawal": "1969-12-31T23:59:59",
          "withdrawn": 0,
          "to_withdraw": 0,
          "withdraw_routes": 0,
          "pending_transfers": 0,
          "curation_rewards": 0,
          "posting_rewards": 0,
          "proxied_vsf_votes": [0, 0, 0, 0],
          "witnesses_voted_for": 0,
          "last_post": "1970-01-01T00:00:00",
          "last_root_post": "1970-01-01T00:00:00",
          "last_post_edit": "1970-01-01T00:00:00",
          "last_vote_time": "1970-01-01T00:00:00",
          "post_bandwidth": 0,
          "pending_claimed_accounts": 0,
          "is_smt": false,
          "delayed_votes": [
            {
              "time": "2021-02-24T05:08:21",
              "val": "11550765516955"
            },
            {
              "time": "2021-02-26T15:46:06",
              "val": "633465684569"
            },
            {
              "time": "2021-03-07T17:54:39",
              "val": "1000000037683"
            },
            {
              "time": "2021-03-16T05:54:33",
              "val": "999978763511"
            },
            {
              "time": "2021-03-18T06:06:00",
              "val": "1000000171317"
            }
          ]
        }
      ]
    }
    

##### Example `curl`[](#database_api.list_accounts-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_accounts", "params": {"start":"", "limit":10, "order":"by_name"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_accounts", "params": {"start":["", ""], "limit":10, "order":"by_proxy"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_accounts", "params": {"start":["1960-01-01T00:00:00", ""], "limit":10, "order":"by_next_vesting_withdrawal","delayed_votes_active":false}, "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF11**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-recovery-request)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.blockchain.html#beem.blockchain.Blockchain.list_change_recovery_account_requests)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=list%20change%20recovery%20account%20requests)**

#### database\_api.list\_change\_recovery\_account\_requests[](#database_api.list_change_recovery_account_requests)

Returns a list of recovery account change requests. Parameters: `start:object`, `limit:int`, `order:string`

*   `start` depends on `order` (see below)
*   `limit` is up to 1000.
*   `order` can be one of:
    *   `by_account` - order by account
        *   `start` is string of: `account`
    *   `by_effective_date` - order by effective date
        *   `start` is an array of two values: `timestamp`, `account`

`start` (object)

`limit` (int)

`order` (string)

 

`""`

10

`"by_account"`

Queries first 10 requests, sort by account

`["1960-01-01T00:00:00", ""]`

10

`"by_effective_date"`

Queries first 10 requests, sort by effective date

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#database_apilist_change_recovery_account_requests)

##### Query Parameters JSON[](#database_api.list_change_recovery_account_requests-parameter_json)

    {"start": null, "limit": 0, "order": "by_name"}
    

##### Expected Response JSON[](#database_api.list_change_recovery_account_requests-expected_response_json)

    {
      "requests": [
        {
          "id": 99,
          "account_to_recover": "alice",
          "recovery_account": "bob",
          "effective_on": "1960-01-01T00:00:00"
        }
      ]
    }
    

##### Example `curl`[](#database_api.list_change_recovery_account_requests-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_change_recovery_account_requests", "params": {"start":"alice", "limit":10, "order":"by_account"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_change_recovery_account_requests", "params": {"start":["1960-01-01T00:00:00",""], "limit":10, "order":"by_effective_date"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=list_comments)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-discussions-by-created)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.comment.html#module-beem.comment)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=list%20comments)**

#### database\_api.list\_comments[](#database_api.list_comments)

Returns all comments, starting with the specified options. Parameters: `start:array`; `limit:int`; `order:string`

*   `start` depends on `order` (see below)
*   `limit` is up to 1000.
*   `order` can be one of:
    *   `by_cashout_time` - order by cashout time
        *   `start` is an array of three required values (two optionally blank): `timestamp`, `author`, `permlink`
    *   `by_permlink` - order by permlink
        *   `start` is an array of two required values (both optionally blank): `author`, `permlink`
    *   `by_root` - order by root
        *   `start` is an array of four required values (two optional blank): `root_author`, `root_permlink`, `child_author`, `child_permlink`
    *   `by_parent` - order by parent
        *   `start` is an array of four required values (two optional blank): `parent_author`, `parent_permlink`, `child_author`, `child_permlink`
    *   `by_last_update` - order by last update
        *   `start` is an array of four required values (two optionally blank): `parent_author`, `update_time`, `start_author`, `permlink`
    *   `by_author_last_update` - order by author’s last update
        *   `start` is an array of four required values (two optionally blank): `parent_author`, `update_time`, `start_author`, `permlink`

`start` (array)

`limit` (int)

`order` (string)

 

`["1970-01-01T00:00:00", "", ""]`

10

`"by_cashout_time"`

Queries first 10 comments, sort by cashout time

`["", ""]`

10

`"by_permlink"`

Queries first 10 comments, sort by permlink

`["hiveio","announcing-the-launch-of-hive-blockchain", "", ""]`

10

`"by_root"`

Queries next 10 comments starting at @hiveio/firstpost, sort by root

`["hiveio","announcing-the-launch-of-hive-blockchain", "", ""]`

10

`"by_parent"`

Queries next 10 comments starting at @hiveio/firstpost, sort by parent

`["hiveio","1970-01-01T00:00:00", "", ""]`

10

`"by_last_update"`

Queries next 10 comments starting at @hiveio’s updates since timpstamp, sort by last update

`["hiveio","1970-01-01T00:00:00", "", ""]`

10

`"by_author_last_update"`

Queries next 10 comments starting at @hiveio’s updates since timestamp, sort by author’s last update

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#database_apilist_comments)

##### Query Parameters JSON[](#database_api.list_comments-parameter_json)

    {"start": null, "limit": 0, "order": "by_name"}
    

##### Expected Response JSON[](#database_api.list_comments-expected_response_json)

    {
      "comments": [
        {
          "active": "2020-03-18T16:45:21",
          "author_rewards": 11835,
          "id": 96448425,
          "author": "berniesanders",
          "permlink": "q7d2ue",
          "category": "communityfork",
          "title": "",
          "body": "https://media.giphy.com/media/xjLlSxM5Z61FJh9wMC/giphy.gif",
          "json_metadata": "{\"image\":[\"https://media.giphy.com/media/xjLlSxM5Z61FJh9wMC/giphy.gif\"],\"app\":\"steemit/0.2\"}",
          "created": "2020-03-17T23:35:06",
          "last_update": "2020-03-17T23:35:06",
          "depth": 1,
          "children": 5,
          "last_payout": "2020-03-24T23:35:06",
          "cashout_time": "1969-12-31T23:59:59",
          "max_cashout_time": "1969-12-31T23:59:59",
          "curator_payout_value": {
            "amount": "2120",
            "nai": "@@000000013",
            "precision": 3
          },
          "total_payout_value": {
            "amount": "2247",
            "nai": "@@000000013",
            "precision": 3
          },
          "reward_weight": 10000,
          "root_author": "hiveio",
          "root_permlink": "announcing-the-launch-of-hive-blockchain",
          "allow_replies": true,
          "allow_votes": true,
          "allow_curation_rewards": true,
          "parent_author": "hiveio",
          "parent_permlink": "announcing-the-launch-of-hive-blockchain",
          "beneficiaries": [],
          "max_accepted_payout": {
            "amount": "1000000000",
            "nai": "@@000000013",
            "precision": 3
          },
          "percent_hbd": 10000,
          "net_votes": 30,
          "total_vote_weight": 0,
          "vote_rshares": 0,
          "net_rshares": 0,
          "abs_rshares": 0,
          "children_abs_rshares": 0
        }
      ]
    }
    

##### Example `curl`[](#database_api.list_comments-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_comments", "params": {"start":["1970-01-01T00:00:00","",""], "limit":10, "order":"by_cashout_time"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_comments", "params": {"start":["",""], "limit":10, "order":"by_permlink"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_comments", "params": {"start":["hiveio","announcing-the-launch-of-hive-blockchain","",""], "limit":10, "order":"by_root"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_comments", "params": {"start":["hiveio","announcing-the-launch-of-hive-blockchain","",""], "limit":10, "order":"by_parent"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_comments", "params": {"start":["hiveio","1970-01-01T00:00:00","",""], "limit":10, "order":"by_last_update"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_comments", "params": {"start":["hiveio","1970-01-01T00:00:00","",""], "limit":10, "order":"by_author_last_update"}, "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF14**
*   **SDK Reference**
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=list%20decline%20voting%20rights%20requests)**

#### database\_api.list\_decline\_voting\_rights\_requests[](#database_api.list_decline_voting_rights_requests)

Returns a list of decline voting rights requests. Parameters: `start:object`; `limit:int`; `order:string`

*   `start` depends on `order` (see below)
*   `limit` is up to 1000.
*   `order` can be one of:
    *   `by_account` - order by account
        *   `start` is a string: `account`
    *   `by_effective_date` - order by effective date
        *   `start` is an array of two values: `timestamp`, `account`

`start` (object)

`limit` (int)

`order` (string)

 

`""`

10

`"by_account"`

Queries first 10 requests, sort by account

`["1960-01-01T00:00:00", ""]`

10

`"by_effective_date"`

Queries first 10 requests, sort by effective date

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#database_apilist_decline_voting_rights_requests)

##### Query Parameters JSON[](#database_api.list_decline_voting_rights_requests-parameter_json)

    {"start": null, "limit": 0, "order": "by_name"}
    

##### Expected Response JSON[](#database_api.list_decline_voting_rights_requests-expected_response_json)

    {"requests": []}
    

##### Example `curl`[](#database_api.list_decline_voting_rights_requests-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_decline_voting_rights_requests", "params": {"start":"", "limit":10, "order":"by_account"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_decline_voting_rights_requests", "params": {"start":["1970-01-01T00:00:00","",""], "limit":10, "order":"by_effective_date"}, "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF14**
*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=list_escrows)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-escrow)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.account.html#beem.account.Account.get_escrow)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=list%20escrows)**

#### database\_api.list\_escrows[](#database_api.list_escrows)

Returns a list of escrows. Parameters: `start:array`; `limit:int`; `order:string`

*   `start` depends on `order` (see below)
*   `limit` is up to 1000.
*   `order` can be one of:
    *   `by_from_id` - order by id
        *   `start` is an array of two values: `account`, `escrow_id`
    *   `by_ratification_deadline` - order by ratification deadline
        *   `start` is an array of three values: `is_approved`, `timestamp`, `escrow_id`

`start` (array)

`limit` (int)

`order` (string)

 

`["alice", 99]`

10

`"by_from_id"`

Queries first 10 requests, sort by id

`[true, "1960-01-01T00:00:00", 99]`

10

`"by_ratification_deadline"`

Queries first 10 requests, sort by ratification deadline

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#database_apilist_escrows)

##### Query Parameters JSON[](#database_api.list_escrows-parameter_json)

    {"start": null, "limit": 0, "order": "by_name"}
    

##### Expected Response JSON[](#database_api.list_escrows-expected_response_json)

    {
      "escrows": [
        {
          "id": 158,
          "escrow_id": 1,
          "from": "addicttolife",
          "to": "fundition.help",
          "agent": "ongame",
          "ratification_deadline": "2018-11-23T17:31:26",
          "escrow_expiration": "2018-11-24T17:31:26",
          "hbd_balance": {
            "amount": "0",
            "precision": 3,
            "nai": "@@000000013"
          },
          "hive_balance": {
            "amount": "4832",
            "precision": 3,
            "nai": "@@000000021"
          },
          "pending_fee": {
            "amount": "0",
            "precision": 3,
            "nai": "@@000000021"
          },
          "to_approved": true,
          "agent_approved": true,
          "disputed": false
        }
      ]
    }
    

##### Example `curl`[](#database_api.list_escrows-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_escrows", "params": {"start":["",0], "limit":10, "order":"by_from_id"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_escrows", "params": {"start":[true, "1970-01-01T00:00:00", 0], "limit":10, "order":"by_ratification_deadline"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=list_limit_orders)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=list%20limit%20orders)**

#### database\_api.list\_limit\_orders[](#database_api.list_limit_orders)

Returns a list of limit orders. Parameters: `start:array`; `limit:int`; `order:string`

*   `start` depends on `order` (see below)
*   `limit` is up to 1000.
*   `order` can be one of:
    *   `by_price` - order by price
        *   `start` is an array of two values: `price`, `order_type`
    *   `by_account` - order by account
        *   `start` is an array of two values: `account`, `order_id`

`start` (array)

`limit` (int)

`order` (string)

 

`[{"base": {"amount": "85405", "precision": 3, "nai": "@@000000021"}, "quote": {"amount": "17192", "precision": 3, "nai": "@@000000013"}}, 0]`

10

`"by_price"`

Queries first 10 requests, sort by price

`["alice", 0]`

10

`"by_account"`

Queries first 10 requests, sort by account

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#database_apilist_limit_orders)

##### Query Parameters JSON[](#database_api.list_limit_orders-parameter_json)

    {"start": null, "limit": 0, "order": "by_name"}
    

##### Expected Response JSON[](#database_api.list_limit_orders-expected_response_json)

    {
      "orders": [
        {
          "id": 3155591,
          "created": "2018-12-05T06:34:21",
          "expiration": "2018-12-15T06:34:20",
          "seller": "teamsmooth-mm",
          "orderid": 2000,
          "for_sale": 197714,
          "sell_price": {
            "base": {
              "amount": "198513",
              "precision": 3,
              "nai": "@@000000021"
            },
            "quote": {
              "amount": "80000",
              "precision": 3,
              "nai": "@@000000013"
            }
          }
        }
      ]
    }
    

##### Example `curl`[](#database_api.list_limit_orders-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_limit_orders", "params": {"start":[{"base":{"amount":"1000","precision":3,"nai":"@@000000021"},"quote":{"amount":"1","precision":3,"nai":"@@000000013"}},0], "limit":10, "order":"by_price"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_limit_orders", "params": {"start":["alice",0], "limit":10, "order":"by_account"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hivexplorer](https://hivexplorer.com/api-docs?q=list_owner_histories)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-owner-history)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.account.html#beem.account.Account.get_owner_history)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=list%20owner%20histories)**

#### database\_api.list\_owner\_histories[](#database_api.list_owner_histories)

Returns a list of owner authority histories. Parameters: `start:array`, `limit:int`

`start` (array)

`limit` (int)

 

`["hiveio", "1970-01-01T00:00:00"]`

10

Queries the owner history starting from account named “hiveio” on “1970-01-01T00:00:00”, limit 10 results.

`["alice", "1970-01-01T00:00:00"]`

10

Queries the owner history starting from account named “alice”, limit 10 results.

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#database_apilist_owner_histories)

##### Query Parameters JSON[](#database_api.list_owner_histories-parameter_json)

    {"start": null, "limit": 0}
    

##### Expected Response JSON[](#database_api.list_owner_histories-expected_response_json)

    {
      "owner_auths": [
        {
          "id": 129742,
          "account": "a-m",
          "previous_owner_authority": {
            "weight_threshold": 1,
            "account_auths": [],
            "key_auths": [
              [
                "STM7J6gXoztfTscNzmzL11DFtTPCFCTeZzsFtFxsQrQw91KnN1YxQ",
                1
              ]
            ]
          },
          "last_valid_time": "2018-11-24T02:35:27"
        }
      ]
    }
    

##### Example `curl`[](#database_api.list_owner_histories-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_owner_histories", "params": {"start":["hiveio","1970-01-01T00:00:00"], "limit":10}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_owner_histories", "params": {"start":["alice","1970-01-01T00:00:00"], "limit":10}, "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF14**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-savings-withdraw-from)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.account.html#beem.account.Account.get_savings_withdrawals)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=list%20savings%20withdrawals)**

#### database\_api.list\_savings\_withdrawals[](#database_api.list_savings_withdrawals)

Returns a list of savings withdrawls. Parameters: `start:object`, `limit:int`, `order:string`

*   `limit` is up to 1000.
*   `order` can be one of:
    *   `by_from_id` - order by id
        *   `start` is an array of two values: `account`, `request_id`
    *   `by_complete_from_id` - order by id (complete)
        *   `start` is an array of three values: `timestamp`, `account`, `request_id`
    *   `by_to_complete` - order by complete
        *   `start` is an array of three values: `account`, `timestamp`, `order_id`

`start` (object)

`limit` (int)

`order` (string)

 

`[0]`

`10`

`"by_from_id"`

Queries the savings withdraw for id.

`["2018-12-07T16:54:03", "hiveio", 0]`

`10`

`"by_complete_from_id"`

Queries the savings withdraw for id (completed).

`["", "1970-01-01T00:00:00", 0]`

`10`

`"by_to_complete"`

Queries the savings withdraw completed.

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#database_apilist_savings_withdrawals)

##### Query Parameters JSON[](#database_api.list_savings_withdrawals-parameter_json)

    {"start": null, "limit": 0, "order": "by_name"}
    

##### Expected Response JSON[](#database_api.list_savings_withdrawals-expected_response_json)

    {
      "withdrawals": [
        {
          "id": 120083,
          "from": "adafnnys",
          "to": "adafnnys",
          "memo": "",
          "request_id": 1543942411,
          "amount": {
            "amount": "2413",
            "precision": 3,
            "nai": "@@000000013"
          },
          "complete": "2018-12-07T16:54:03"
        }
      ]
    }
    

##### Example `curl`[](#database_api.list_savings_withdrawals-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_savings_withdrawals", "params": {"start":[0], "limit":10, "order":"by_from_id"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_savings_withdrawals", "params": {"start":["2018-12-07T16:54:03", "hiveio", 0], "limit":10, "order":"by_complete_from_id"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_savings_withdrawals", "params": {"start":["", "1970-01-01T00:00:00", 0], "limit":10, "order":"by_to_complete"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-conversion-requests)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.account.html#beem.account.Account.get_conversion_requests)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=list%20hbd%20conversion%20requests)**

#### database\_api.list\_hbd\_conversion\_requests[](#database_api.list_hbd_conversion_requests)

Returns the list of HBD conversion requests for an account. Parameters: `start:array`, `limit:int`, `order:string`

*   `limit` is up to 1000.
*   `order` can be one of:
    *   `by_account` - order by accont name
        *   `start` is an array of two values: `account`, `request_id`
    *   `by_conversion_date` - order by conversion date
        *   `start` is an array of two values: `timestamp`, `request_id`

`start` (array)

`limit` (int)

`order` (string)

 

`["hiveio", 0]`

10

`by_account`

Queries a conversion request for hiveio, limit to 10 results, order by account name.

`["2018-12-07T16:54:03", 0]`

10

`by_conversion_date`

Queries a conversion request from this date, limit to 10 results, order by conversion date.

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#database_apilist_hbd_conversion_requests)

##### Query Parameters JSON[](#database_api.list_hbd_conversion_requests-parameter_json)

    {"start": null, "limit": 0, "order": "by_name"}
    

##### Expected Response JSON[](#database_api.list_hbd_conversion_requests-expected_response_json)

    {
      "requests": [
        {
          "id": 75677,
          "owner": "adenijiadeshina",
          "requestid": 3,
          "amount": {
            "amount": "311",
            "precision": 3,
            "nai": "@@000000013"
          },
          "conversion_date": "2018-12-06T20:42:42"
        }
      ]
    }
    

##### Example `curl`[](#database_api.list_hbd_conversion_requests-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_hbd_conversion_requests", "params": {"start":["hiveio", 0], "limit":10, "order":"by_account"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_hbd_conversion_requests", "params": {"start":["2018-12-07T16:54:03", 0], "limit":10, "order":"by_conversion_date"}, "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF17**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-vesting-delegations)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.account.html#beem.account.Account.get_expiring_vesting_delegations)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/delegations)
    
*   **[Related](/search/?q=list%20vesting%20delegation%20expirations)**

#### database\_api.list\_vesting\_delegation\_expirations[](#database_api.list_vesting_delegation_expirations)

Returns a list of vesting delegation expirations. Parameters: `start:array`, `limit:int`, `order:string`

*   `limit` is up to 1000.
*   `order` can be one of:
    *   `by_expiration` - order by expiration
        *   `start` is an array of two values: `timestamp`, `expiration_id`
    *   `by_account_expiration` - order by account expiration
        *   `start` is an array of two values: `account`, `timestamp`, `expiration_id`

`start` (array)

`limit` (int)

`order` (string)

 

`["1970-01-01T00:00:00", 0]`

10

`by_expiration`

Queries delegations, limit to 10 results, order by expiration.

`["alice", "1970-01-01T00:00:00", 0]`

10

`by_account_expiration`

Queries delegation from this date, limit to 10 results, order by account expiration.

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#database_apilist_vesting_delegation_expirations)

##### Query Parameters JSON[](#database_api.list_vesting_delegation_expirations-parameter_json)

    {"start": null, "limit": 0, "order": "by_name"}
    

##### Expected Response JSON[](#database_api.list_vesting_delegation_expirations-expected_response_json)

    {
      "delegations": [
        {
          "id": 3076685,
          "delegator": "anonsteem",
          "vesting_shares": {
            "amount": "6050629930",
            "precision": 6,
            "nai": "@@000000037"
          },
          "expiration": "2018-12-05T07:07:15"
        }
      ]
    }
    

##### Example `curl`[](#database_api.list_vesting_delegation_expirations-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_vesting_delegation_expirations", "params": {"start":["1970-01-01T00:00:00",0], "limit":10, "order":"by_expiration"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_vesting_delegation_expirations", "params": {"start":["alice", "1970-01-01T00:00:00",0], "limit":10, "order":"by_account_expiration"}, "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF17**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-vesting-delegations)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.account.html#beem.account.Account.get_expiring_vesting_delegations)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/delegations)
    
*   **[Related](/search/?q=list%20vesting%20delegations)**

#### database\_api.list\_vesting\_delegations[](#database_api.list_vesting_delegations)

Returns a list of vesting delegations. Parameters: `start:array`, `limit:int`, `order:string`

*   `limit` is up to 1000.
*   `order` can be one of:
    *   `by_delegation` - order by delegations
        *   `start` is an array of two values: `delegator`, `delegatee`

`start` (array)

`limit` (int)

`order` (string)

 

`["", ""]`

10

`by_delegation`

Queries delegations, limit to 10 results, order by delegations.

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#database_apilist_vesting_delegations)

##### Query Parameters JSON[](#database_api.list_vesting_delegations-parameter_json)

    {"start": null, "limit": 0, "order": "by_name"}
    

##### Expected Response JSON[](#database_api.list_vesting_delegations-expected_response_json)

    {
      "delegations": [
        {
          "id": 554317,
          "delegator": "a-0-0-0",
          "delegatee": "a-0-0",
          "vesting_shares": {
            "amount": "6141067173",
            "precision": 6,
            "nai": "@@000000037"
          },
          "min_delegation_time": "2018-01-24T22:23:54"
        }
      ]
    }
    

##### Example `curl`[](#database_api.list_vesting_delegations-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_vesting_delegations", "params": {"start":["",""], "limit":10, "order":"by_delegation"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-account-votes)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.vote.html#beem.vote.AccountVotes)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=list%20votes)**

#### database\_api.list\_votes[](#database_api.list_votes)

Returns all votes, starting with the specified voter and/or author and permlink. Parameters: `start:array`; `limit:int`; `order:string`

*   `start` depends on `order` (see below)
    *   `voter` is optional
    *   `author` and `permlink` are optional, but if one is blank, they must both be blank
*   `limit` is up to 1000.
*   `order` can be one of:
    *   `by_comment_voter` - order by comment voter
        *   `start` is an array of three optional values: `author`, `permlink`, `voter`
    *   `by_voter_comment` - order by voter comment
        *   `start` is an array of three optional values: `voter`, `author`, `permlink`

`start` (array)

`limit` (int)

`order` (string)

 

`["", "", ""]`

10

`"by_comment_voter"`

Queries first 10 votes, sort by comment voter

`["", "", ""]`

10

`"by_voter_comment"`

Queries first 10 votes, sort by voter comment

`["xeroc", "vanteem-config", ""]`

10

`"by_comment_voter"`

Queries next 10 votes starting on the post `@xeroc/vanteem-config`, sort by comment voter

`["alice", "xeroc", "vanteem-config"]`

10

`"by_voter_comment"`

Queries next 10 votes starting at alice on the post `@xeroc/vanteem-config`, sort by voter comment

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#database_apilist_votes)

##### Query Parameters JSON[](#database_api.list_votes-parameter_json)

    {
      "start": null,
      "limit": 0,
      "order": "by_comment_voter"
    }
    

##### Expected Response JSON[](#database_api.list_votes-expected_response_json)

    {
      "votes": [
        {
          "id": 9,
          "voter": "dantheman",
          "author": "hiveio",
          "permlink": "firstpost",
          "weight": "32866333630",
          "rshares": 375241,
          "vote_percent": 100,
          "last_update": "2016-04-07T19:15:36",
          "num_changes": -1
        }
      ]
    }
    

##### Example `curl`[](#database_api.list_votes-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_votes", "params": {"start":["", "", ""], "limit":10, "order":"by_comment_voter"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_votes", "params": {"start":["", "", ""], "limit":10, "order":"by_voter_comment"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_votes", "params": {"start":["", "", "hiveio"], "limit":10, "order":"by_comment_voter"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_votes", "params": {"start":["alice", "xeroc", "vanteem-config"], "limit":10, "order":"by_voter_comment"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-withdraw-routes)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.account.html#beem.account.Account.withdraw_vesting)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=list%20withdraw%20vesting%20routes)**

#### database\_api.list\_withdraw\_vesting\_routes[](#database_api.list_withdraw_vesting_routes)

Returns a list of vesting withdraw routes. Parameters: `start:array`; `limit:int`; `order:string`

*   `start` depends on `order` (see below)
*   `limit` is up to 1000.
*   `order` can be one of:
    *   `by_withdraw_route` - order by withdraw route
        *   `start` is an array of two values: `from_account`, `to_account`
    *   `by_destination` - order by destination
        *   `start` is an array of two values: `to_account`, `route_id`

`start` (array)

`limit` (int)

`order` (string)

 

`["temp", ""]`

10

`"by_withdraw_route"`

Queries first 10 routes, sort by withdraw route

`["", 0]`

10

`"by_destination"`

Queries first 10 routes, sort by destination

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#database_apilist_withdraw_vesting_routes)

##### Query Parameters JSON[](#database_api.list_withdraw_vesting_routes-parameter_json)

    {"start": null, "limit": 0, "order": "by_name"}
    

##### Expected Response JSON[](#database_api.list_withdraw_vesting_routes-expected_response_json)

    {
      "routes": [
        {
          "id": 39503,
          "from_account": "temperature",
          "to_account": "luckdiver",
          "percent": 10000,
          "auto_vest": false
        }
      ]
    }
    

##### Example `curl`[](#database_api.list_withdraw_vesting_routes-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_withdraw_vesting_routes", "params": {"start":["temp",""], "limit":10, "order":"by_withdraw_route"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_withdraw_vesting_routes", "params": {"start":["",0], "limit":10, "order":"by_destination"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-witnesses-by-vote)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.witness.html#beem.witness.WitnessesRankedByVote)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/witnesses)
    
*   **[Related](/search/?q=list%20witness%20votes)**

#### database\_api.list\_witness\_votes[](#database_api.list_witness_votes)

Returns a list of witness votes. Parameters: `start:array`; `limit:int`; `order:string`

*   `start` depends on `order` (see below)
*   `limit` is up to 1000.
*   `order` can be one of:
    *   `by_account_witness` - order by account witness
        *   `start` is an array of two values: `account`, `witness`
    *   `by_witness_account` - order by witness account
        *   `start` is an array of two values: `witness`, `account`

`start` (array)

`limit` (int)

`order` (string)

 

`["", ""]`

10

`"by_withdraw_route"`

Queries first 10 votes, sort by account witness

`["", ""]`

10

`"by_destination"`

Queries first 10 votes, sort by witness account

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#database_apilist_witness_votes)

##### Query Parameters JSON[](#database_api.list_witness_votes-parameter_json)

    {"start": null, "limit": 0, "order": "by_name"}
    

##### Expected Response JSON[](#database_api.list_witness_votes-expected_response_json)

    {
      "votes": [
        {
          "id": 428961,
          "witness": "aggroed",
          "account": "a-0magic"
        }
      ]
    }
    

##### Example `curl`[](#database_api.list_witness_votes-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_witness_votes", "params": {"start":["",""], "limit":10, "order":"by_account_witness"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_witness_votes", "params": {"start":["",""], "limit":10, "order":"by_witness_account"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-witnesses-by-vote)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.witness.html#beem.witness.WitnessesRankedByVote)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/witnesses)
    
*   **[Related](/search/?q=list%20witnesses)**

#### database\_api.list\_witnesses[](#database_api.list_witnesses)

Returns the list of witnesses. Parameters: `start:object`; `limit:int`; `order:string`

*   `start` depends on `order` (see below)
*   `limit` is up to 1000.
*   `order` can be one of:
    *   `by_name` - order by name
        *   `start` is string value: `account`
    *   `by_vote_name` - order by vote, name
        *   `start` is an array of two values: `votes`, `account`
    *   `by_schedule_time` - order by schedule time
        *   `start` is an array of two values: `virtual_scheduled_time`, `account`

`start` (object)

`limit` (int)

`order` (string)

 

`""`

10

`"by_name"`

Queries first 10 witnesses, sort by account name

`[0, ""]`

10

`"by_vote_name"`

Queries first 10 witnesses, sort by votes

`["473718186844702107410533306", "alice"]`

10

`"by_schedule_time"`

Queries first 10 witnesses, sort by schedule

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#database_apilist_witnesses)

##### Query Parameters JSON[](#database_api.list_witnesses-parameter_json)

    {"start": null, "limit": 0, "order": "by_name"}
    

##### Expected Response JSON[](#database_api.list_witnesses-expected_response_json)

    {
      "witnesses": [
        {
          "id": 6950,
          "owner": "a-0",
          "created": "1970-01-01T00:00:00",
          "url": "",
          "votes": 0,
          "virtual_last_update": "0",
          "virtual_position": "0",
          "virtual_scheduled_time": "340282366920938463463374607431768211455",
          "total_missed": 0,
          "last_aslot": 1063323,
          "last_confirmed_block_num": 1040423,
          "pow_worker": 0,
          "signing_key": "STM5RrTRNDhhrMaA24SzSeE5AvmUcutb1q1VZp1imnT8p871s3UjN",
          "props": {
            "account_creation_fee": {
              "amount": "1",
              "precision": 3,
              "nai": "@@000000021"
            },
            "maximum_block_size": 131072,
            "hbd_interest_rate": 1000,
            "account_subsidy_budget": 797,
            "account_subsidy_decay": 347321
          },
          "hbd_exchange_rate": {
            "base": {
              "amount": "0",
              "precision": 3,
              "nai": "@@000000021"
            },
            "quote": {
              "amount": "0",
              "precision": 3,
              "nai": "@@000000021"
            }
          },
          "last_hbd_exchange_update": "1970-01-01T00:00:00",
          "last_work": "000000127cb0e335667f30100bc1a061175c2d789f808e0e9ac82ee70fa8e604",
          "running_version": "0.0.0",
          "hardfork_version_vote": "0.0.0",
          "hardfork_time_vote": "2016-03-24T16:00:00",
          "available_witness_account_subsidies": 0
        }
      ]
    }
    

##### Example `curl`[](#database_api.list_witnesses-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_witnesses", "params": {"start":"", "limit":10, "order":"by_name"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_witnesses", "params": {"start":[0,""], "limit":10, "order":"by_vote_name"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_witnesses", "params": {"start":["473718186844702107410533306","alice"], "limit":10, "order":"by_schedule_time"}, "id":1}' https://api.hive.blog
    

* * *

*   **Disabled**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#verify-account-authority)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.account.html#beem.account.Account.verify_account_authority)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=verify%20account%20authority)**

#### database\_api.verify\_account\_authority[](#database_api.verify_account_authority)

**Not Implemented**

##### Query Parameters JSON[](#database_api.verify_account_authority-parameter_json)

    {"account": "", "signers": []}
    

##### Expected Response JSON[](#database_api.verify_account_authority-expected_response_json)

    {"valid": false}
    

##### Example `curl`[](#database_api.verify_account_authority-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.verify_account_authority", "params":{"account":"temp","signers":["STM8GC13uCZbP44HzMLV6zPZGwVQ8Nt4Kji8PapsPiNq1BK153XTX"]}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#verify-authority)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html#beem.transactionbuilder.TransactionBuilder.verify_authority)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=verify%20authority)**

#### database\_api.verify\_authority[](#database_api.verify_authority)

Returns true if the transaction has all of the required signatures, otherwise throws an exception.

##### Query Parameters JSON[](#database_api.verify_authority-parameter_json)

    {
      "trx": {
        "ref_block_num": 0,
        "ref_block_prefix": 0,
        "expiration": "1970-01-01T00:00:00",
        "operations": [],
        "extensions": [],
        "signatures": []
      },
      "pack": "legacy"
    }
    

##### Expected Response JSON[](#database_api.verify_authority-expected_response_json)

    {"valid": false}
    

##### Example `curl`[](#database_api.verify_authority-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.verify_authority", "params":{"trx":{"ref_block_num":1097,"ref_block_prefix":2181793527,"expiration":"2016-03-24T18:00:21","operations":[{"type":"pow_operation","value":{"worker_account":"cloop3","block_id":"00000449f7860b82b4fbe2f317c670e9f01d6d9a","nonce":3899,"work":{"worker":"STM7P5TDnA87Pj9T4mf6YHrhzjC1KbPZpNxLWCcVcHxNYXakpoT4F","input":"ae8e7c677119d22385f8c48026fee7aad7bba693bf788d7f27047f40b47738c0","signature":"1f38fe9a3f9989f84bd94aa5bbc88beaf09b67f825aa4450cf5105d111149ba6db560b582c7dbb026c7fc9c2eb5051815a72b17f6896ed59d3851d9a0f9883ca7a","work":"000e7b209d58f2e64b36e9bf12b999c6c7af168cc3fc41eb7f8a4bf796c174c3"},"props":{"account_creation_fee":{"amount":"100000","precision":3,"nai":"@@000000021"},"maximum_block_size":131072,"hbd_interest_rate":1000}}}],"extensions":[],"signatures":[]}}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=verify%20signatures)**

#### database\_api.verify\_signatures[](#database_api.verify_signatures)

This method validates if transaction was signed by person listed in required\_owner, required\_active or required\_posting parameter. `Hash` is a mix of chain\_id and transaction data.

##### Query Parameters JSON[](#database_api.verify_signatures-parameter_json)

    {
      "hash": "0000000000000000000000000000000000000000000000000000000000000000",
      "signatures": [],
      "required_owner": [],
      "required_active": [],
      "required_posting": [],
      "required_other": []
    }
    

##### Expected Response JSON[](#database_api.verify_signatures-expected_response_json)

    {"valid": false}
    

##### Example `curl`[](#database_api.verify_signatures-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.verify_signatures", "params":{"hash": "0000000000000000000000000000000000000000000000000000000000000000", "signatures": [], "required_owner": [], "required_active": [], "required_posting": [], "required_other": []}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/proposals)
    
*   **[Related](/search/?q=find%20proposals)**

#### database\_api.find\_proposals[](#database_api.find_proposals)

Finds proposals by `proposal.id` (not `proposal.proposal_id`).

##### Query Parameters JSON[](#database_api.find_proposals-parameter_json)

    {"proposal_ids": [0]}
    

##### Expected Response JSON[](#database_api.find_proposals-expected_response_json)

    {
      "proposals": [
        {
          "id": 0,
          "proposal_id": "139925218365120",
          "creator": "alice",
          "receiver": "bob",
          "start_date": "2019-07-01T00:00:00",
          "end_date": "2019-08-01T23:59:59",
          "daily_pay": {
            "amount": "4800000",
            "precision": 3,
            "nai": "@@000000013"
          },
          "subject": "My Proposal",
          "permlink": "creator-proposal-permlink",
          "total_votes": "77351826710",
          "status": "active"
        }
      ]
    }
    

##### Example `curl`[](#database_api.find_proposals-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.find_proposals", "params":{"proposal_ids": [0]}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/proposalsapprovals)
    
*   **[Related](/search/?q=list%20proposal%20votes)**

#### database\_api.list\_proposal\_votes[](#database_api.list_proposal_votes)

Returns all proposal votes, starting with the specified voter or `proposal.id`. Parameters: `start:array`; `limit:int`; `order:string`; `order_direction:string`; `status:string`

*   `start` depends on `order` (see below)
    *   `voter` - voter of the proposal (account name string)
    *   `proposal.id` - id the proposal (int)
*   `limit` is up to 1000.
*   `order` can be one of:
    *   `by_voter_proposal` - order by proposal voter
    *   `by_proposal_voter` - order by `proposal.id`
*   `order_direction` can be one of:
    *   `ascending`
    *   `descending`
*   `status`
    *   `all`
    *   `inactive`
    *   `active`
    *   `expired`
    *   `votable`

`start` (array)

`limit` (int)

`order` (string)

`order_direction` (string)

`status` (string)

 

`["alice"]`

10

`by_voter_proposal`

`ascending`

`active`

list 10 proposals with active status, ordered by voter, ascending

`[10]`

1000

`by_proposal_voter`

`ascending`

`votable`

list 1000 votes on proposal 10, ordered by `proposal.id`, ascending

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#database_apilist_proposal_votes)

##### Query Parameters JSON[](#database_api.list_proposal_votes-parameter_json)

    {
      "start": null,
      "limit": 0,
      "order": "by_name",
      "order_direction": "ascending",
      "status": "all"
    }
    

##### Expected Response JSON[](#database_api.list_proposal_votes-expected_response_json)

    {
      "proposal_votes": [
        {
          "id": 0,
          "voter": "charlie",
          "proposal": {
            "id": 0,
            "proposal_id": 0,
            "creator": "alice",
            "receiver": "bob",
            "start_date": "2019-07-01T00:00:00",
            "end_date": "2019-08-01T23:59:59",
            "daily_pay": {
              "amount": "4800000",
              "precision": 3,
              "nai": "@@000000013"
            },
            "subject": "My Proposal",
            "permlink": "creator-proposal-permlink",
            "total_votes": "77351826710",
            "status": "active"
          }
        }
      ]
    }
    

##### Example `curl`[](#database_api.list_proposal_votes-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_proposal_votes", "params":{"start": [""], "limit": 10, "order": "by_voter_proposal", "order_direction": "ascending", "status": "active"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_proposal_votes", "params":{"start": [0], "limit": 10, "order": "by_proposal_voter", "order_direction": "ascending", "status": "active"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/proposals)
    
*   **[Related](/search/?q=list%20proposals)**

#### database\_api.list\_proposals[](#database_api.list_proposals)

Returns all proposals, starting with the specified creator or start date. Parameters: `start:array`; `limit:int`; `order:string`; `order_direction:string`; `status:string`

*   `start` depends on `order` (see below)
    *   `creator` - creator of the proposal (account name string)
    *   `start_date` - start date of the proposal (date string)
    *   `end_date` - end date of the proposal (date string)
    *   `total_votes` - total votes of the proposal (int)
*   `limit` is up to 1000.
*   `order` can be one of:
    *   `by_creator` - order by proposal creator
    *   `by_start_date` - order by proposal start date
    *   `by_end_date` - order by proposal end date
    *   `by_total_votes` - order by proposal total votes
*   `order_direction` can be one of:
    *   `ascending`
    *   `descending`
*   `status`
    *   `all`
    *   `inactive`
    *   `active`
    *   `expired`
    *   `votable`
*   `last_id (optional) - Id of the last object in the previous page from which you should start listing the next page`

`start` (array)

`limit` (int)

`order` (string)

`order_direction` (string)

`status` (string)

 

`[""]`

10

`by_creator`

`ascending`

`active`

list 10 proposals with active status, ordered by creator, ascending

`["2019-08-07T16:54:03"]`

1000

`by_start_date`

`ascending`

`inactive`

list 1000 proposals with inactive status, ordered by start date, ascending, since 2019-08-07T16:54:03

`["a"]`

1

`by_creator`

`ascending`

`expired`

list 1 proposal with expired status, ordered by creator, ascending, by accounts starting with “a”

`["alice"]`

10

`by_creator`

`ascending`

`all`

list 10 proposals with any status, ordered by creator, ascending, by alice

`[""]`

1000

`by_creator`

`ascending`

`votable`

list 1000 votable proposals, ordered by creator, ascending

`[10]`

1000

`by_total_votes`

`ascending`

`votable`

list 1000 votable proposals, ordered by creator, ascending, having at least 10 votes

##### Proposal Structure:

*   `id` - Unique identifier that is mostly an implementation detail (best to ignore). To uniquely identify proposal, it's best to use `proposal_id`.
*   `proposal_id` - Before using this value for any further broadcasts, ensure it is part of an irreversible block.
*   `creator` - Account that created this proposal.
*   `receiver` - Account that will receive funds, if this proposal is approved.
*   `start_date` - When payments should begin.
*   `end_date` - When payments should end.
*   `daily_pay` - Amount of HBD expected per day.
*   `subject` - Summary of this proposal.
*   `permlink` - Post by either creator or receiver.
*   `total_votes` - VESTS cast for this proposal. This will is calculate every maintenance period.
*   `status` - Current status of this proposal.

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#database_apilist_proposals)

##### Query Parameters JSON[](#database_api.list_proposals-parameter_json)

    {
      "start": null,
      "limit": 0,
      "order": "by_name",
      "order_direction": "ascending",
      "status": "all"
    }
    

##### Expected Response JSON[](#database_api.list_proposals-expected_response_json)

    {
      "proposals": [
        {
          "id": 0,
          "proposal_id": "1103806595072",
          "creator": "alice",
          "receiver": "bob",
          "start_date": "2019-07-01T00:00:00",
          "end_date": "2019-08-01T23:59:59",
          "daily_pay": {
            "amount": "4800000",
            "precision": 3,
            "nai": "@@000000013"
          },
          "subject": "My Proposal",
          "permlink": "creator-proposal-permlink",
          "total_votes": "77351826710",
          "status": "active"
        }
      ]
    }
    

##### Example `curl`[](#database_api.list_proposals-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_proposals", "params":{"start": [""], "limit": 10, "order": "by_creator", "order_direction": "ascending", "status": "active"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_proposals", "params":{"start": ["2019-08-07T16:54:03"], "limit": 1000, "order": "by_start_date", "order_direction": "ascending", "status": "inactive"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_proposals", "params":{"start": ["a"], "limit": 1, "order": "by_creator", "order_direction": "ascending", "status": "expired"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_proposals", "params":{"start": ["alice"], "limit": 10, "order": "by_creator", "order_direction": "ascending", "status": "all"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_proposals", "params":{"start": [""], "limit": 1000, "order": "by_creator", "order_direction": "ascending", "status": "votable"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.list_proposals", "params":{"start": [10], "limit": 1000, "order": "by_total_votes", "order_direction": "ascending", "status": "votable"}, "id":1}' https://api.hive.blog
    

* * *

*   **[Related](/search/?q=get%20comment%20pending%20payouts)**

#### database\_api.get\_comment\_pending\_payouts[](#database_api.get_comment_pending_payouts)

Get comment pending payout data.

**Parameters:**

*   `comments` - author/permlink

`comments` (array:string)

 

`[["hbd.funder", "upvote-this-post-to-fund-hbdstabilizer-qr2j7n"]]`

Returns comment info for a single post.

`[["hbd.funder", "upvote-this-post-to-fund-hbdstabilizer-qr2j7n"], ["arcange", "hivesql-proposal-unfunded-information-and-reaction"]]`

Returns comment info for multiple posts.

##### Query Parameters JSON[](#database_api.get_comment_pending_payouts-parameter_json)

    {
      "comments": [
        [
          "hbd.funder",
          "upvote-this-post-to-fund-hbdstabilizer-qr2j7n"
        ]
      ]
    }
    

##### Expected Response JSON[](#database_api.get_comment_pending_payouts-expected_response_json)

    {
      "cashout_infos": [
        {
          "author": "hbd.funder",
          "permlink": "upvote-this-post-to-fund-hbdstabilizer-qr2j7n",
          "cashout_info": {
            "total_vote_weight": 22841196,
            "total_payout_value": {
              "amount": "0",
              "precision": 3,
              "nai": "@@000000013"
            },
            "curator_payout_value": {
              "amount": "0",
              "precision": 3,
              "nai": "@@000000013"
            },
            "max_accepted_payout": {
              "amount": "1000000000",
              "precision": 3,
              "nai": "@@000000013"
            },
            "author_rewards": 0,
            "children_abs_rshares": "606511906476641",
            "net_rshares": "571577939879762",
            "abs_rshares": "594467432989642",
            "vote_rshares": "583007369825359",
            "net_votes": 378,
            "active": "2021-04-06T15:29:03",
            "last_payout": "1970-01-01T00:00:00",
            "cashout_time": "2021-04-12T02:07:00",
            "max_cashout_time": "1969-12-31T23:59:59",
            "percent_hbd": 10000,
            "reward_weight": 10000,
            "allow_replies": false,
            "allow_votes": true,
            "allow_curation_rewards": true
          }
        }
      ]
    }
    

##### Example `curl`[](#database_api.get_comment_pending_payouts-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.get_comment_pending_payouts", "params":{"comments":[["hbd.funder", "upvote-this-post-to-fund-hbdstabilizer-qr2j7n"]]}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.get_comment_pending_payouts", "params":{"comments":[["hbd.funder", "upvote-this-post-to-fund-hbdstabilizer-qr2j7n"], ["arcange", "hivesql-proposal-unfunded-information-and-reaction"]]}, "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF25**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/database-diagram#blocks-and-transactions)
    
*   **[Related](/search/?q=known%20transaction)**

#### database\_api.is\_known\_transaction[](#database_api.is_known_transaction)

Only return true _if_ the transaction has not expired or been invalidated. If this method is called with a VERY old transaction we will return false, use `account_history_api.get_transaction`.

Also see: [transaction\_status\_api.find\_transaction](/apidefinitions/#transaction_status_api.find_transaction), [account\_history\_api.get\_transaction](/apidefinitions/#account_history_api.get_transaction)

##### Query Parameters JSON[](#database_api.is_known_transaction-parameter_json)

    {"id": "0000000000000000000000000000000000000000"}
    

##### Expected Response JSON[](#database_api.is_known_transaction-expected_response_json)

    {"is_known": false}
    

##### Example `curl`[](#database_api.is_known_transaction-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.is_known_transaction", "params":{"id":"0000000000000000000000000000000000000000"}, "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF25**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/-/blob/master/doc/README.md#collateralized-convert)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txcollateralizedconverts-hf25)
    
*   **[Related](/search/?q=find%20collateralized%20conversion%20requests)**

#### database\_api.find\_collateralized\_conversion\_requests[](#database_api.find_collateralized_conversion_requests)

Returns objects corresponding with `collateralized_convert` operations.

##### Query Parameters JSON[](#database_api.find_collateralized_conversion_requests-parameter_json)

    {"account": ""}
    

##### Expected Response JSON[](#database_api.find_collateralized_conversion_requests-expected_response_json)

    {"requests": []}
    

* * *

*   **Since: HF25**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/-/blob/master/doc/README.md#collateralized-convert)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txcollateralizedconverts-hf25)
    
*   **[Related](/search/?q=list%20collateralized%20conversion%20requests)**

#### database\_api.list\_collateralized\_conversion\_requests[](#database_api.list_collateralized_conversion_requests)

Returns objects corresponding with `collateralized_convert` operations.

##### Query Parameters JSON[](#database_api.list_collateralized_conversion_requests-parameter_json)

    {"start": null, "limit": 0, "order": "by_name"}
    

##### Expected Response JSON[](#database_api.list_collateralized_conversion_requests-expected_response_json)

    {"requests": []}
    

* * *

*   **Since: HF25**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txrecurrenttransfers-hf25)
    
*   **[Related](/search/?q=find%20recurrent%20transfers)**

#### database\_api.find\_recurrent\_transfers[](#database_api.find_recurrent_transfers)

Finds transfers of any liquid asset every fixed amount of time from one account to another.

Also see: [recurrent\_transfer\_operation](/apidefinitions/#broadcast_ops_recurrent_transfer)

##### Query Parameters JSON[](#database_api.find_recurrent_transfers-parameter_json)

    {"from": ""}
    

##### Expected Response JSON[](#database_api.find_recurrent_transfers-expected_response_json)

    {
      "recurrent_transfers": [
        {
          "id": 3,
          "trigger_date": "2021-07-02T18:11:51",
          "from": "alice",
          "to": "bob",
          "amount": {
            "amount": "1000",
            "precision": 3,
            "nai": "@@000000021"
          },
          "memo": "Payroll",
          "recurrence": 26,
          "consecutive_failures": 0,
          "remaining_executions": 3
        }
      ]
    }
    

##### Example `curl`[](#database_api.find_recurrent_transfers-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"database_api.find_recurrent_transfers", "params":{"from":"alice"}, "id":1}' https://api.hive.blog
    

* * *

### Debug Node API

Methods:

*   [debug\_generate\_blocks](#debug_node_api.debug_generate_blocks)
*   [debug\_generate\_blocks\_until](#debug_node_api.debug_generate_blocks_until)
*   [debug\_get\_hardfork\_property\_object](#debug_node_api.debug_get_hardfork_property_object)
*   [debug\_get\_json\_schema](#debug_node_api.debug_get_json_schema)
*   [debug\_get\_witness\_schedule](#debug_node_api.debug_get_witness_schedule)
*   [debug\_has\_hardfork](#debug_node_api.debug_has_hardfork)
*   [debug\_pop\_block](#debug_node_api.debug_pop_block)
*   [debug\_push\_blocks](#debug_node_api.debug_push_blocks)
*   [debug\_set\_hardfork](#debug_node_api.debug_set_hardfork)

This plugin allows all sorts of creative “what-if” experiments with the chain.

See: [debug\_node\_plugin.md](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/debug_node_plugin.md)

*   **SDK Reference**
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=debug%20generate%20blocks)**

#### debug\_node\_api.debug\_generate\_blocks[](#debug_node_api.debug_generate_blocks)

Generate blocks locally.

##### Query Parameters JSON[](#debug_node_api.debug_generate_blocks-parameter_json)

    {
      "debug_key": "",
      "count": 0,
      "skip": 0,
      "miss_blocks": 0,
      "edit_if_needed": true
    }
    

##### Expected Response JSON[](#debug_node_api.debug_generate_blocks-expected_response_json)

    {"blocks": 0}
    

* * *

*   **SDK Reference**
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=debug%20generate%20blocks)**

#### debug\_node\_api.debug\_generate\_blocks\_until[](#debug_node_api.debug_generate_blocks_until)

Generate blocks locally until a specified head block time. Can generate them sparsely.

##### Query Parameters JSON[](#debug_node_api.debug_generate_blocks_until-parameter_json)

    {
      "debug_key": "",
      "head_block_time": "1970-01-01T00:00:00",
      "generate_sparsely": true
    }
    

##### Expected Response JSON[](#debug_node_api.debug_generate_blocks_until-expected_response_json)

    {"blocks": 0}
    

* * *

*   **SDK Reference**
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=debug%20get%20hardfork%20property%20object)**

#### debug\_node\_api.debug\_get\_hardfork\_property\_object[](#debug_node_api.debug_get_hardfork_property_object)

##### Query Parameters JSON[](#debug_node_api.debug_get_hardfork_property_object-parameter_json)

    {}
    

##### Expected Response JSON[](#debug_node_api.debug_get_hardfork_property_object-expected_response_json)

    {
      "id": 0,
      "processed_hardforks": [],
      "last_hardfork": 0,
      "current_hardfork_version": "0.0.0",
      "next_hardfork": "0.0.0",
      "next_hardfork_time": "1970-01-01T00:00:00"
    }
    

* * *

*   **SDK Reference**
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=debug%20get%20json%20schema)**

#### debug\_node\_api.debug\_get\_json\_schema[](#debug_node_api.debug_get_json_schema)

##### Query Parameters JSON[](#debug_node_api.debug_get_json_schema-parameter_json)

    {}
    

##### Expected Response JSON[](#debug_node_api.debug_get_json_schema-expected_response_json)

    {"schema": ""}
    

* * *

*   **SDK Reference**
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=debug%20get%20witness%20schedule)**

#### debug\_node\_api.debug\_get\_witness\_schedule[](#debug_node_api.debug_get_witness_schedule)

##### Query Parameters JSON[](#debug_node_api.debug_get_witness_schedule-parameter_json)

    {}
    

##### Expected Response JSON[](#debug_node_api.debug_get_witness_schedule-expected_response_json)

    {
      "id": 0,
      "current_virtual_time": "0",
      "next_shuffle_block_num": 21573344,
      "current_shuffled_witnesses": [],
      "num_scheduled_witnesses": 192,
      "elected_weight": 49,
      "timeshare_weight": 73,
      "miner_weight": 1,
      "witness_pay_normalization_factor": 0,
      "median_props": {
        "account_creation_fee": {
          "amount": "0",
          "precision": 3,
          "nai": "@@000000021"
        },
        "maximum_block_size": 131072,
        "hbd_interest_rate": 1000,
        "account_subsidy_budget": 797,
        "account_subsidy_decay": 347321
      },
      "majority_version": "0.0.0",
      "max_voted_witnesses": 128,
      "max_miner_witnesses": 131,
      "max_runner_witnesses": 191,
      "hardfork_required_witnesses": 4,
      "account_subsidy_rd": {
        "resource_unit": 0,
        "budget_per_time_unit": 0,
        "pool_eq": 0,
        "max_pool_size": 0,
        "decay_params": {
          "decay_per_time_unit": 0,
          "decay_per_time_unit_denom_shift": 0
        },
        "min_decay": 0
      },
      "account_subsidy_witness_rd": {
        "resource_unit": 0,
        "budget_per_time_unit": 0,
        "pool_eq": 0,
        "max_pool_size": 0,
        "decay_params": {
          "decay_per_time_unit": 0,
          "decay_per_time_unit_denom_shift": 0
        },
        "min_decay": 0
      },
      "min_witness_account_subsidy_decay": 0
    }
    

* * *

*   **SDK Reference**
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=debug%20hardfork)**

#### debug\_node\_api.debug\_has\_hardfork[](#debug_node_api.debug_has_hardfork)

##### Query Parameters JSON[](#debug_node_api.debug_has_hardfork-parameter_json)

    {"hardfork_id": 0}
    

##### Expected Response JSON[](#debug_node_api.debug_has_hardfork-expected_response_json)

    {"has_hardfork": false}
    

* * *

*   **SDK Reference**
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=debug%20pop%20block)**

#### debug\_node\_api.debug\_pop\_block[](#debug_node_api.debug_pop_block)

Pop a block from the blockchain, returning it.

##### Query Parameters JSON[](#debug_node_api.debug_pop_block-parameter_json)

    {}
    

##### Expected Response JSON[](#debug_node_api.debug_pop_block-expected_response_json)

    {}
    

* * *

*   **SDK Reference**
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=debug%20push%20blocks)**

#### debug\_node\_api.debug\_push\_blocks[](#debug_node_api.debug_push_blocks)

Push blocks from existing database.

##### Query Parameters JSON[](#debug_node_api.debug_push_blocks-parameter_json)

    {
      "src_filename": "",
      "count": 0,
      "skip_validate_invariants": false
    }
    

##### Expected Response JSON[](#debug_node_api.debug_push_blocks-expected_response_json)

    {"blocks": 0}
    

* * *

*   **SDK Reference**
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=debug%20set%20hardfork)**

#### debug\_node\_api.debug\_set\_hardfork[](#debug_node_api.debug_set_hardfork)

##### Query Parameters JSON[](#debug_node_api.debug_set_hardfork-parameter_json)

    {"hardfork_id": 0}
    

##### Expected Response JSON[](#debug_node_api.debug_set_hardfork-expected_response_json)

    {}
    

* * *

### Follow API

Methods:

*   [get\_account\_reputations](#follow_api.get_account_reputations)
*   [get\_blog](#follow_api.get_blog)
*   [get\_blog\_authors](#follow_api.get_blog_authors)
*   [get\_blog\_entries](#follow_api.get_blog_entries)
*   [get\_feed](#follow_api.get_feed)
*   [get\_feed\_entries](#follow_api.get_feed_entries)
*   [get\_follow\_count](#follow_api.get_follow_count)
*   [get\_followers](#follow_api.get_followers)
*   [get\_following](#follow_api.get_following)
*   [get\_reblogged\_by](#follow_api.get_reblogged_by)

Used to lookup information related to reputation and account follow operations. **These AppBase API methods are still under development and subject to change.**

*   **Since: HF13**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-account-reputations)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-account-reputations)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20account%20reputations)**

#### follow\_api.get\_account\_reputations[](#follow_api.get_account_reputations)

Returns a list of account reputations.

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#follow_apiget_account_reputations)

##### Query Parameters JSON[](#follow_api.get_account_reputations-parameter_json)

    {"account_lower_bound": "", "limit": 1000}
    

##### Expected Response JSON[](#follow_api.get_account_reputations-expected_response_json)

    {
      "reputations": [{"account": "", "reputation": 0}]
    }
    

##### Example `curl`[](#follow_api.get_account_reputations-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"follow_api.get_account_reputations", "params":{"account_lower_bound":"hiveio", "limit":1}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"follow_api.get_account_reputations", "params":{"account_lower_bound":"a", "limit":10}, "id":1}' https://api.hive.blog
    

* * *

*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-blog)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-blog)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20blog)**

#### follow\_api.get\_blog[](#follow_api.get_blog)

**Removed since HF24** Use: [`condenser_api.get_blog`](/apidefinitions/#condenser_api.get_blog)

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#condenser_apiget_blog)

* * *

*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-blog-authors)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-blog-authors)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20blog%20authors)**

#### follow\_api.get\_blog\_authors[](#follow_api.get_blog_authors)

**Removed since HF24** Use: [`condenser_api.get_blog_authors`](/apidefinitions/#condenser_api.get_blog_authors)

* * *

*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-blog-entries)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-blog-entries)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20blog%20entries)**

#### follow\_api.get\_blog\_entries[](#follow_api.get_blog_entries)

**Removed since HF24** Use: [`condenser_api.get_blog_entries`](/apidefinitions/#condenser_api.get_blog_entries)

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#condenser_apiget_blog_entries)

* * *

*   **Since: HF14**
*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-feed-entries)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-feed)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20feed)**

#### follow\_api.get\_feed[](#follow_api.get_feed)

**Removed since HF24** Use: [`condenser_api.get_feed`](/apidefinitions/#condenser_api.get_feed)

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#condenser_apiget_feed)

* * *

*   **Since: HF14**
*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-feed-entries)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-feed-entries)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20feed%20entries)**

#### follow\_api.get\_feed\_entries[](#follow_api.get_feed_entries)

**Removed since HF24** Use: [`condenser_api.get_feed_entries`](/apidefinitions/#condenser_api.get_feed_entries)

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#condenser_apiget_feed_entries)

</p>

* * *

*   **Since: HF9**
*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-follow-count)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-follow-count)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/followers)
    
*   **[Related](/search/?q=get%20follow%20count)**

#### follow\_api.get\_follow\_count[](#follow_api.get_follow_count)

**Removed since HF24** Use: [`condenser_api.get_follow_count`](/apidefinitions/#condenser_api.get_follow_count)

* * *

*   **Since: HF9**
*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-followers)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-followers)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/followers)
    
*   **[Related](/search/?q=get%20followers)**

#### follow\_api.get\_followers[](#follow_api.get_followers)

**Removed since HF24** Use: [`condenser_api.get_followers`](/apidefinitions/#condenser_api.get_followers)

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#condenser_apiget_followers)

* * *

*   **Since: HF9**
*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-following)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-following)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/followers)
    
*   **[Related](/search/?q=get%20following)**

#### follow\_api.get\_following[](#follow_api.get_following)

**Removed since HF24** Use: [`condenser_api.get_following`](/apidefinitions/#condenser_api.get_following)

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#condenser_apiget_following)

* * *

*   **Since: HF14**
*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-reblogged-by)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-reblogged-by)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
    [hivesql](https://docs.hivesql.io/technical-informations/state-tables/reblogs)
    
*   **[Related](/search/?q=get%20reblogged)**

#### follow\_api.get\_reblogged\_by[](#follow_api.get_reblogged_by)

**Removed since HF24** Use: [`condenser_api.get_reblogged_by`](/apidefinitions/#condenser_api.get_reblogged_by)

* * *

### JSON RPC

Methods:

*   [get\_methods](#jsonrpc.get_methods)
*   [get\_signature](#jsonrpc.get_signature)

Used to lookup information about the JSON RPC API. **These AppBase API methods are still under development and subject to change.**

*   **SDK Reference**
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20methods)**

#### jsonrpc.get\_methods[](#jsonrpc.get_methods)

Returns a list of methods supported by the JSON RPC API.

##### Query Parameters JSON[](#jsonrpc.get_methods-parameter_json)

    {}
    

##### Expected Response JSON[](#jsonrpc.get_methods-expected_response_json)

    [
      "account_by_key_api.get_key_references",
      "account_history_api.enum_virtual_ops",
      "account_history_api.get_account_history",
      "account_history_api.get_ops_in_block",
      "account_history_api.get_transaction",
      "block_api.get_block",
      "block_api.get_block_header",
      "condenser_api.broadcast_block",
      "condenser_api.broadcast_transaction",
      "condenser_api.broadcast_transaction_synchronous",
      "condenser_api.find_proposals",
      "condenser_api.get_account_count",
      "condenser_api.get_account_history",
      "condenser_api.get_account_references",
      "condenser_api.get_account_reputations",
      "condenser_api.get_account_votes",
      "condenser_api.get_accounts",
      "condenser_api.get_active_votes",
      "condenser_api.get_active_witnesses",
      "condenser_api.get_block",
      "condenser_api.get_block_header",
      "condenser_api.get_blog",
      "condenser_api.get_blog_authors",
      "condenser_api.get_blog_entries",
      "condenser_api.get_chain_properties",
      "condenser_api.get_comment_discussions_by_payout",
      "condenser_api.get_config",
      "condenser_api.get_content",
      "condenser_api.get_content_replies",
      "condenser_api.get_conversion_requests",
      "condenser_api.get_current_median_history_price",
      "condenser_api.get_discussions_by_active",
      "condenser_api.get_discussions_by_author_before_date",
      "condenser_api.get_discussions_by_blog",
      "condenser_api.get_discussions_by_cashout",
      "condenser_api.get_discussions_by_children",
      "condenser_api.get_discussions_by_comments",
      "condenser_api.get_discussions_by_created",
      "condenser_api.get_discussions_by_feed",
      "condenser_api.get_discussions_by_hot",
      "condenser_api.get_discussions_by_promoted",
      "condenser_api.get_discussions_by_trending",
      "condenser_api.get_discussions_by_votes",
      "condenser_api.get_dynamic_global_properties",
      "condenser_api.get_escrow",
      "condenser_api.get_expiring_vesting_delegations",
      "condenser_api.get_feed",
      "condenser_api.get_feed_entries",
      "condenser_api.get_feed_history",
      "condenser_api.get_follow_count",
      "condenser_api.get_followers",
      "condenser_api.get_following",
      "condenser_api.get_hardfork_version",
      "condenser_api.get_key_references",
      "condenser_api.get_market_history",
      "condenser_api.get_market_history_buckets",
      "condenser_api.get_nai_pool",
      "condenser_api.get_next_scheduled_hardfork",
      "condenser_api.get_open_orders",
      "condenser_api.get_ops_in_block",
      "condenser_api.get_order_book",
      "condenser_api.get_owner_history",
      "condenser_api.get_post_discussions_by_payout",
      "condenser_api.get_potential_signatures",
      "condenser_api.get_reblogged_by",
      "condenser_api.get_recent_trades",
      "condenser_api.get_recovery_request",
      "condenser_api.get_replies_by_last_update",
      "condenser_api.get_required_signatures",
      "condenser_api.get_reward_fund",
      "condenser_api.get_savings_withdraw_from",
      "condenser_api.get_savings_withdraw_to",
      "condenser_api.get_state",
      "condenser_api.get_tags_used_by_author",
      "condenser_api.get_ticker",
      "condenser_api.get_trade_history",
      "condenser_api.get_transaction",
      "condenser_api.get_transaction_hex",
      "condenser_api.get_trending_tags",
      "condenser_api.get_version",
      "condenser_api.get_vesting_delegations",
      "condenser_api.get_volume",
      "condenser_api.get_withdraw_routes",
      "condenser_api.get_witness_by_account",
      "condenser_api.get_witness_count",
      "condenser_api.get_witness_schedule",
      "condenser_api.get_witnesses",
      "condenser_api.get_witnesses_by_vote",
      "condenser_api.list_proposal_votes",
      "condenser_api.list_proposals",
      "condenser_api.lookup_account_names",
      "condenser_api.lookup_accounts",
      "condenser_api.lookup_witness_accounts",
      "condenser_api.verify_account_authority",
      "condenser_api.verify_authority",
      "database_api.find_account_recovery_requests",
      "database_api.find_accounts",
      "database_api.find_change_recovery_account_requests",
      "database_api.find_comments",
      "database_api.find_decline_voting_rights_requests",
      "database_api.find_escrows",
      "database_api.find_limit_orders",
      "database_api.find_owner_histories",
      "database_api.find_proposals",
      "database_api.find_savings_withdrawals",
      "database_api.find_hbd_conversion_requests",
      "database_api.find_smt_contributions",
      "database_api.find_smt_token_emissions",
      "database_api.find_smt_tokens",
      "database_api.find_vesting_delegation_expirations",
      "database_api.find_vesting_delegations",
      "database_api.find_votes",
      "database_api.find_withdraw_vesting_routes",
      "database_api.find_witnesses",
      "database_api.get_active_witnesses",
      "database_api.get_config",
      "database_api.get_current_price_feed",
      "database_api.get_dynamic_global_properties",
      "database_api.get_feed_history",
      "database_api.get_hardfork_properties",
      "database_api.get_nai_pool",
      "database_api.get_order_book",
      "database_api.get_potential_signatures",
      "database_api.get_required_signatures",
      "database_api.get_reward_funds",
      "database_api.get_transaction_hex",
      "database_api.get_version",
      "database_api.get_witness_schedule",
      "database_api.list_account_recovery_requests",
      "database_api.list_accounts",
      "database_api.list_change_recovery_account_requests",
      "database_api.list_comments",
      "database_api.list_decline_voting_rights_requests",
      "database_api.list_escrows",
      "database_api.list_limit_orders",
      "database_api.list_owner_histories",
      "database_api.list_proposal_votes",
      "database_api.list_proposals",
      "database_api.list_savings_withdrawals",
      "database_api.list_hbd_conversion_requests",
      "database_api.list_smt_contributions",
      "database_api.list_smt_token_emissions",
      "database_api.list_smt_tokens",
      "database_api.list_vesting_delegation_expirations",
      "database_api.list_vesting_delegations",
      "database_api.list_votes",
      "database_api.list_withdraw_vesting_routes",
      "database_api.list_witness_votes",
      "database_api.list_witnesses",
      "database_api.verify_account_authority",
      "database_api.verify_authority",
      "database_api.verify_signatures",
      "follow_api.get_account_reputations",
      "follow_api.get_blog",
      "follow_api.get_blog_authors",
      "follow_api.get_blog_entries",
      "follow_api.get_feed",
      "follow_api.get_feed_entries",
      "follow_api.get_follow_count",
      "follow_api.get_followers",
      "follow_api.get_following",
      "follow_api.get_reblogged_by",
      "jsonrpc.get_methods",
      "jsonrpc.get_signature",
      "market_history_api.get_market_history",
      "market_history_api.get_market_history_buckets",
      "market_history_api.get_order_book",
      "market_history_api.get_recent_trades",
      "market_history_api.get_ticker",
      "market_history_api.get_trade_history",
      "market_history_api.get_volume",
      "network_broadcast_api.broadcast_block",
      "network_broadcast_api.broadcast_transaction",
      "rc_api.find_rc_accounts",
      "rc_api.get_resource_params",
      "rc_api.get_resource_pool",
      "tags_api.get_active_votes",
      "tags_api.get_comment_discussions_by_payout",
      "tags_api.get_content_replies",
      "tags_api.get_discussion",
      "tags_api.get_discussions_by_active",
      "tags_api.get_discussions_by_author_before_date",
      "tags_api.get_discussions_by_blog",
      "tags_api.get_discussions_by_cashout",
      "tags_api.get_discussions_by_children",
      "tags_api.get_discussions_by_comments",
      "tags_api.get_discussions_by_created",
      "tags_api.get_discussions_by_feed",
      "tags_api.get_discussions_by_hot",
      "tags_api.get_discussions_by_promoted",
      "tags_api.get_discussions_by_trending",
      "tags_api.get_discussions_by_votes",
      "tags_api.get_post_discussions_by_payout",
      "tags_api.get_replies_by_last_update",
      "tags_api.get_tags_used_by_author",
      "tags_api.get_trending_tags"
    ]
    

##### Example `curl`[](#jsonrpc.get_methods-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"jsonrpc.get_methods", "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20signature)**

#### jsonrpc.get\_signature[](#jsonrpc.get_signature)

Returns the signature information for a JSON RPC method including the arguments and expected response JSON.

##### Query Parameters JSON[](#jsonrpc.get_signature-parameter_json)

    {"method": ""}
    

##### Expected Response JSON[](#jsonrpc.get_signature-expected_response_json)

    {"args": {}, "ret": []}
    

##### Example `curl`[](#jsonrpc.get_signature-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"jsonrpc.get_signature", "params":{"method":"jsonrpc.get_methods"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"jsonrpc.get_signature", "params":{"method":"jsonrpc.get_signature"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"jsonrpc.get_signature", "params":{"method":"condenser_api.get_dynamic_global_properties"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"jsonrpc.get_signature", "params":{"method":"database_api.get_dynamic_global_properties"}, "id":1}' https://api.hive.blog
    

* * *

### Market History API

Methods:

*   [get\_market\_history](#market_history_api.get_market_history)
*   [get\_market\_history\_buckets](#market_history_api.get_market_history_buckets)
*   [get\_order\_book](#market_history_api.get_order_book)
*   [get\_recent\_trades](#market_history_api.get_recent_trades)
*   [get\_ticker](#market_history_api.get_ticker)
*   [get\_trade\_history](#market_history_api.get_trade_history)
*   [get\_volume](#market_history_api.get_volume)

Used to lookup market history information. **These AppBase API methods are still under development and subject to change.**

*   **SDK Reference**
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-market-history)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20market%20history)**

#### market\_history\_api.get\_market\_history[](#market_history_api.get_market_history)

Returns the market history for the internal HBD:HIVE market.

##### Query Parameters JSON[](#market_history_api.get_market_history-parameter_json)

    {
      "bucket_seconds": 0,
      "start": "1970-01-01T00:00:00",
      "end": "1970-01-01T00:00:00"
    }
    

##### Expected Response JSON[](#market_history_api.get_market_history-expected_response_json)

    {
      "buckets": [
        {
          "id": 0,
          "open": "2019-12-18T01:51:15",
          "seconds": 15,
          "hive": {
            "high": 100000,
            "low": 100000,
            "open": 100000,
            "close": 100000,
            "volume": 100000
          },
          "symbol": {"nai": "@@000000013", "precision": 3},
          "non_hive": {
            "high": 100000,
            "low": 100000,
            "open": 100000,
            "close": 100000,
            "volume": 100000
          }
        }
      ]
    }
    

##### Example `curl`[](#market_history_api.get_market_history-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"market_history_api.get_market_history", "params":{"bucket_seconds":15,"start":"2018-01-01T00:00:00","end":"2018-01-02T00:00:00"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"market_history_api.get_market_history", "params":{"bucket_seconds":60,"start":"2018-01-01T00:00:00","end":"2018-01-02T00:00:00"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"market_history_api.get_market_history", "params":{"bucket_seconds":300,"start":"2018-01-01T00:00:00","end":"2018-01-02T00:00:00"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"market_history_api.get_market_history", "params":{"bucket_seconds":3600,"start":"2018-01-01T00:00:00","end":"2018-01-02T00:00:00"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"market_history_api.get_market_history", "params":{"bucket_seconds":86400,"start":"2018-01-01T00:00:00","end":"2018-01-02T00:00:00"}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-market-history-buckets)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-market-history-buckets)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20market%20history%20buckets)**

#### market\_history\_api.get\_market\_history\_buckets[](#market_history_api.get_market_history_buckets)

Returns the bucket seconds being tracked by the plugin.

##### Query Parameters JSON[](#market_history_api.get_market_history_buckets-parameter_json)

    {}
    

##### Expected Response JSON[](#market_history_api.get_market_history_buckets-expected_response_json)

    {"bucket_sizes": [15, 60, 300, 3600, 86400]}
    

##### Example `curl`[](#market_history_api.get_market_history_buckets-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"market_history_api.get_market_history_buckets", "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-order-book)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-order-book)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20order%20book)**

#### market\_history\_api.get\_order\_book[](#market_history_api.get_order_book)

Returns the internal market order book.

##### Query Parameters JSON[](#market_history_api.get_order_book-parameter_json)

    {"limit": 500}
    

##### Expected Response JSON[](#market_history_api.get_order_book-expected_response_json)

    {
      "bids": [],
      "asks": [
        {
          "order_price": {
            "base": {
              "amount": "1000",
              "precision": 3,
              "nai": "@@000000021"
            },
            "quote": {
              "amount": "100",
              "precision": 6,
              "nai": "@@100042205"
            }
          },
          "real_price": "0.10000000000000001",
          "hive": 100000,
          "hbd": 10000,
          "created": "2019-12-18T01:24:42"
        },
        {
          "order_price": {
            "base": {
              "amount": "1000",
              "precision": 3,
              "nai": "@@000000021"
            },
            "quote": {
              "amount": "1000",
              "precision": 6,
              "nai": "@@100041380"
            }
          },
          "real_price": "1.00000000000000000",
          "hive": 1000,
          "hbd": 1000,
          "created": "2019-12-18T01:22:12"
        },
        {
          "order_price": {
            "base": {
              "amount": "1000",
              "precision": 3,
              "nai": "@@000000021"
            },
            "quote": {
              "amount": "100000000000",
              "precision": 11,
              "nai": "@@100037284"
            }
          },
          "real_price": "100000000.00000000000000000",
          "hive": 1000,
          "hbd": "100000000000",
          "created": "2019-12-18T01:20:21"
        }
      ]
    }
    

##### Example `curl`[](#market_history_api.get_order_book-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"market_history_api.get_order_book", "params":{"limit":10}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"market_history_api.get_order_book", "params":{"limit":50}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-recent-trades)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-recent-trades)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20recent%20trades)**

#### market\_history\_api.get\_recent\_trades[](#market_history_api.get_recent_trades)

Returns the most recent trades for the internal HBD:HIVE market.

##### Query Parameters JSON[](#market_history_api.get_recent_trades-parameter_json)

    {"limit": 1000}
    

##### Expected Response JSON[](#market_history_api.get_recent_trades-expected_response_json)

    {
      "trades": [
        {
          "date": "2019-12-18T01:51:24",
          "current_pays": {
            "amount": "100000",
            "precision": 3,
            "nai": "@@000000013"
          },
          "open_pays": {
            "amount": "100000",
            "precision": 3,
            "nai": "@@000000021"
          }
        }
      ]
    }
    

##### Example `curl`[](#market_history_api.get_recent_trades-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"market_history_api.get_recent_trades", "params":{"limit":10}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"market_history_api.get_recent_trades", "params":{"limit":500}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-ticker)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-ticker)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20ticker)**

#### market\_history\_api.get\_ticker[](#market_history_api.get_ticker)

Returns the market ticker for the internal HBD:HIVE market.

##### Query Parameters JSON[](#market_history_api.get_ticker-parameter_json)

    {}
    

##### Expected Response JSON[](#market_history_api.get_ticker-expected_response_json)

    {
      "latest": "1.00000000000000000",
      "lowest_ask": "0.10000000000000001",
      "highest_bid": "0.00000000000000000",
      "percent_change": "0.00000000000000000",
      "hive_volume": {
        "amount": "100000",
        "precision": 3,
        "nai": "@@000000021"
      },
      "hbd_volume": {
        "amount": "100000",
        "precision": 3,
        "nai": "@@000000013"
      }
    }
    

##### Example `curl`[](#market_history_api.get_ticker-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"market_history_api.get_ticker", "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-trade-history)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-trade-history)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20trade%20history)**

#### market\_history\_api.get\_trade\_history[](#market_history_api.get_trade_history)

Returns the trade history for the internal HBD:HIVE market.

##### Query Parameters JSON[](#market_history_api.get_trade_history-parameter_json)

    {
      "start": "1970-01-01T00:00:00",
      "end": "1970-01-01T00:00:00",
      "limit": 1000
    }
    

##### Expected Response JSON[](#market_history_api.get_trade_history-expected_response_json)

    {
      "trades": [
        {
          "date": "2019-12-18T01:51:24",
          "current_pays": {
            "amount": "100000",
            "precision": 3,
            "nai": "@@000000013"
          },
          "open_pays": {
            "amount": "100000",
            "precision": 3,
            "nai": "@@000000021"
          }
        }
      ]
    }
    

##### Example `curl`[](#market_history_api.get_trade_history-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"market_history_api.get_trade_history", "params":{"start":"2018-01-01T00:00:00","end":"2018-01-02T00:00:00","limit":10}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-volume)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-volume)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20volume)**

#### market\_history\_api.get\_volume[](#market_history_api.get_volume)

Returns the market volume for the past 24 hours.

##### Query Parameters JSON[](#market_history_api.get_volume-parameter_json)

    {}
    

##### Expected Response JSON[](#market_history_api.get_volume-expected_response_json)

    {
      "hive_volume": {
        "amount": "0",
        "precision": 3,
        "nai": "@@000000021"
      },
      "hbd_volume": {
        "amount": "0",
        "precision": 3,
        "nai": "@@000000013"
      }
    }
    

##### Example `curl`[](#market_history_api.get_volume-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"market_history_api.get_volume", "id":1}' https://api.hive.blog
    

* * *

### Network Broadcast API

Methods:

*   [broadcast\_block](#network_broadcast_api.broadcast_block)
*   [broadcast\_transaction](#network_broadcast_api.broadcast_transaction)

Used to broadcast transactions and blocks. **These AppBase API methods are still under development and subject to change.**

Also see: [Blockchain Ops](/apidefinitions/broadcast-ops.html)

*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#broadcast-api)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/TransactionBuilder)
    
*   **[Related](/search/?q=broadcast%20block)**

#### network\_broadcast\_api.broadcast\_block[](#network_broadcast_api.broadcast_block)

**Removed: HF26**

Used to broadcast a block.

##### Query Parameters JSON[](#network_broadcast_api.broadcast_block-parameter_json)

    {
      "block": {
        "previous": "0000000000000000000000000000000000000000",
        "timestamp": "1970-01-01T00:00:00",
        "witness": "",
        "transaction_merkle_root": "0000000000000000000000000000000000000000",
        "extensions": [],
        "witness_signature": "0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000",
        "transactions": []
      }
    }
    

##### Expected Response JSON[](#network_broadcast_api.broadcast_block-expected_response_json)

    {}
    

##### Example `curl`[](#network_broadcast_api.broadcast_block-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"network_broadcast_api.broadcast_block", "params":{"block":{"previous":"0000000000000000000000000000000000000000","timestamp":"1970-01-01T00:00:00","witness":"","transaction_merkle_root":"0000000000000000000000000000000000000000","extensions":[],"witness_signature":"0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000","transactions":[]}}, "id":1}' https://api.hive.blog
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#broadcast-api)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/TransactionBuilder)
    
*   **[Related](/search/?q=broadcast%20transaction)**

#### network\_broadcast\_api.broadcast\_transaction[](#network_broadcast_api.broadcast_transaction)

Used to broadcast a transaction.

##### Query Parameters JSON[](#network_broadcast_api.broadcast_transaction-parameter_json)

    {
      "trx": {
        "ref_block_num": 0,
        "ref_block_prefix": 0,
        "expiration": "1970-01-01T00:00:00",
        "operations": [],
        "extensions": [],
        "signatures": []
      },
      "max_block_age": -1
    }
    

##### Expected Response JSON[](#network_broadcast_api.broadcast_transaction-expected_response_json)

    {}
    

##### Example `curl`[](#network_broadcast_api.broadcast_transaction-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"network_broadcast_api.broadcast_transaction", "params":{"trx":{"ref_block_num":1097,"ref_block_prefix":2181793527,"expiration":"2016-03-24T18:00:21","operations":[{"type":"vote_operation","value":{"voter":"hiveio","author":"alice","permlink":"a-post-by-alice","weight":10000}}],"extensions":[],"signatures":[]},"max_block_age":50}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"network_broadcast_api.broadcast_transaction", "params":{"trx":{"ref_block_num":1097,"ref_block_prefix":2181793527,"expiration":"2016-03-24T18:00:21","operations":[{"type":"pow_operation","value":{"worker_account":"cloop3","block_id":"00000449f7860b82b4fbe2f317c670e9f01d6d9a","nonce":3899,"work":{"worker":"STM7P5TDnA87Pj9T4mf6YHrhzjC1KbPZpNxLWCcVcHxNYXakpoT4F","input":"ae8e7c677119d22385f8c48026fee7aad7bba693bf788d7f27047f40b47738c0","signature":"1f38fe9a3f9989f84bd94aa5bbc88beaf09b67f825aa4450cf5105d111149ba6db560b582c7dbb026c7fc9c2eb5051815a72b17f6896ed59d3851d9a0f9883ca7a","work":"000e7b209d58f2e64b36e9bf12b999c6c7af168cc3fc41eb7f8a4bf796c174c3"},"props":{"account_creation_fee":{"amount":"100000","precision":3,"nai":"@@000000021"},"maximum_block_size":131072,"hbd_interest_rate":1000}}}],"extensions":[],"signatures":[]},"max_block_age":50}, "id":1}' https://api.hive.blog
    

* * *

### RC API

Methods:

*   [find\_rc\_accounts](#rc_api.find_rc_accounts)
*   [get\_resource\_params](#rc_api.get_resource_params)
*   [get\_resource\_pool](#rc_api.get_resource_pool)
*   [list\_rc\_accounts](#rc_api.list_rc_accounts)
*   [list\_rc\_direct\_delegations](#rc_api.list_rc_direct_delegations)

Allows querying of various Resource Credit metrics. See: [RC Bandwidth System](/tutorials-recipes/rc-bandwidth-system.html), [0.20.2 Release Notes](https://archive.is/1T93t), [Developer Guide: Resource Credit System](https://hive.blog/steem/@steemitdev/developer-guide-resource-credit-system)

*   **Since: HF20**
*   **SDK Reference**
    
    [beem](https://beem.readthedocs.io/en/latest/beem.rc.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=find%20rc%20accounts)**

#### rc\_api.find\_rc\_accounts[](#rc_api.find_rc_accounts)

Returns the available resource credits of accounts. Parameters: `accounts:string array`

`accounts` (string)

 

`"hiveio"`

Query the available resource credits for the account named “hiveio”.

`"alice"`

Query the available resource credits for the accounts named “alice” and “bob”.

##### Query Parameters JSON[](#rc_api.find_rc_accounts-parameter_json)

    {"accounts": []}
    

##### Expected Response JSON[](#rc_api.find_rc_accounts-expected_response_json)

    {
      "rc_accounts": [
        {
          "account": "",
          "rc_manabar": {"current_mana": "0", "last_update_time": 0},
          "max_rc_creation_adjustment": {
            "amount": "0",
            "precision": 6,
            "nai": "@@000000037"
          },
          "max_rc": "0"
        }
      ]
    }
    

##### Example `curl`[](#rc_api.find_rc_accounts-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"rc_api.find_rc_accounts", "params":{"accounts":["hiveio"]}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"rc_api.find_rc_accounts", "params":{"accounts":["alice","bob"]}, "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF20**
*   **SDK Reference**
    
    [beem](https://beem.readthedocs.io/en/latest/beem.rc.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20resource%20params)**

#### rc\_api.get\_resource\_params[](#rc_api.get_resource_params)

Exports all relevant resource size constants, in particular the measurement-based execution time parameters.

See: [#2980](https://archive.ph/p88d2)

##### Query Parameters JSON[](#rc_api.get_resource_params-parameter_json)

    {}
    

##### Expected Response JSON[](#rc_api.get_resource_params-expected_response_json)

    {
      "resource_names": [
        "resource_history_bytes",
        "resource_new_accounts",
        "resource_market_bytes",
        "resource_state_bytes",
        "resource_execution_time"
      ],
      "resource_params": {
        "resource_history_bytes": {
          "resource_dynamics_params": {
            "resource_unit": 1,
            "budget_per_time_unit": 43403,
            "pool_eq": "27050539251",
            "max_pool_size": "54101078501",
            "decay_params": {
              "decay_per_time_unit": 3613026481,
              "decay_per_time_unit_denom_shift": 51
            },
            "min_decay": 0
          },
          "price_curve_params": {
            "coeff_a": "14034213032882683904",
            "coeff_b": 211332338,
            "shift": 52
          }
        },
        "resource_new_accounts": {
          "resource_dynamics_params": {
            "resource_unit": 10000,
            "budget_per_time_unit": 797,
            "pool_eq": 157691079,
            "max_pool_size": 157691079,
            "decay_params": {
              "decay_per_time_unit": 347321,
              "decay_per_time_unit_denom_shift": 36
            },
            "min_decay": 0
          },
          "price_curve_params": {
            "coeff_a": "16484671763857882971",
            "coeff_b": 1231961,
            "shift": 51
          }
        },
        "resource_market_bytes": {
          "resource_dynamics_params": {
            "resource_unit": 10,
            "budget_per_time_unit": 72338,
            "pool_eq": 2003755169,
            "max_pool_size": 4007510337,
            "decay_params": {
              "decay_per_time_unit": 2540365427,
              "decay_per_time_unit_denom_shift": 46
            },
            "min_decay": 0
          },
          "price_curve_params": {
            "coeff_a": "9979884823383242752",
            "coeff_b": 15654337,
            "shift": 56
          }
        },
        "resource_state_bytes": {
          "resource_dynamics_params": {
            "resource_unit": 1,
            "budget_per_time_unit": 34722222,
            "pool_eq": "21640431400373",
            "max_pool_size": "43280862800744",
            "decay_params": {
              "decay_per_time_unit": 3613026481,
              "decay_per_time_unit_denom_shift": 51
            },
            "min_decay": 0
          },
          "price_curve_params": {
            "coeff_a": "14034213032882683904",
            "coeff_b": "169065870315",
            "shift": 52
          }
        },
        "resource_execution_time": {
          "resource_dynamics_params": {
            "resource_unit": 1,
            "budget_per_time_unit": 10273973,
            "pool_eq": "6403196140384",
            "max_pool_size": "12806392280766",
            "decay_params": {
              "decay_per_time_unit": 3613026481,
              "decay_per_time_unit_denom_shift": 51
            },
            "min_decay": 0
          },
          "price_curve_params": {
            "coeff_a": "14034213032882683904",
            "coeff_b": "50024969847",
            "shift": 52
          }
        }
      },
      "size_info": {
        "resource_state_bytes": {
          "authority_base_size": 40000,
          "authority_account_member_size": 180000,
          "authority_key_member_size": 350000,
          "account_object_base_size": 4800000,
          "account_authority_object_base_size": 400000,
          "account_recovery_request_object_base_size": 320000,
          "comment_object_base_size": 2010000,
          "comment_object_permlink_char_size": 10000,
          "comment_object_parent_permlink_char_size": 20000,
          "comment_object_beneficiaries_member_size": 180000,
          "comment_vote_object_base_size": 24675,
          "convert_request_object_base_size": 480000,
          "decline_voting_rights_request_object_base_size": 280000,
          "escrow_object_base_size": 1190000,
          "limit_order_object_base_size": 147440,
          "savings_withdraw_object_byte_size": 14656,
          "transaction_object_base_size": 6090,
          "transaction_object_byte_size": 174,
          "vesting_delegation_object_base_size": 600000,
          "vesting_delegation_expiration_object_base_size": 440000,
          "withdraw_vesting_route_object_base_size": 430000,
          "witness_object_base_size": 2660000,
          "witness_object_url_char_size": 10000,
          "witness_vote_object_base_size": 400000,
          "proposal_object_base_size": 680000,
          "proposal_vote_object_base_size": 240000,
          "proposal_vote_object_member_size": 80000,
          "smt_token_object_size": 2400000,
          "smt_ico_object_size": 403520,
          "smt_token_emissions_object_size": 1040000,
          "smt_ico_tier_object_size": 186240,
          "smt_contribution_object_size": 108640,
          "votable_assets_item_size": 200000,
          "STATE_BYTES_SCALE": 10000
        },
        "resource_execution_time": {
          "account_create_operation_exec_time": 57700,
          "account_create_with_delegation_operation_exec_time": 57700,
          "account_update_operation_exec_time": 14000,
          "account_update2_operation_exec_time": 14000,
          "account_witness_proxy_operation_exec_time": 117000,
          "account_witness_vote_operation_exec_time": 23000,
          "cancel_transfer_from_savings_operation_exec_time": 11500,
          "change_recovery_account_operation_exec_time": 12000,
          "claim_account_operation_exec_time": 10000,
          "claim_reward_balance_operation_exec_time": 50300,
          "comment_operation_exec_time": 114100,
          "comment_options_operation_exec_time": 13200,
          "convert_operation_exec_time": 15700,
          "create_claimed_account_operation_exec_time": 57700,
          "custom_operation_exec_time": 11400,
          "custom_json_operation_exec_time": 11400,
          "custom_binary_operation_exec_time": 11400,
          "decline_voting_rights_operation_exec_time": 5300,
          "delegate_vesting_shares_operation_exec_time": 19900,
          "delete_comment_operation_exec_time": 51100,
          "escrow_approve_operation_exec_time": 9900,
          "escrow_dispute_operation_exec_time": 11500,
          "escrow_release_operation_exec_time": 17200,
          "escrow_transfer_operation_exec_time": 19100,
          "feed_publish_operation_exec_time": 6200,
          "limit_order_cancel_operation_exec_time": 9600,
          "limit_order_create_operation_exec_time": 31700,
          "limit_order_create2_operation_exec_time": 31700,
          "request_account_recovery_operation_exec_time": 54400,
          "set_withdraw_vesting_route_operation_exec_time": 17900,
          "transfer_from_savings_operation_exec_time": 17500,
          "transfer_operation_exec_time": 9600,
          "transfer_to_savings_operation_exec_time": 6400,
          "transfer_to_vesting_operation_exec_time": 44400,
          "vote_operation_exec_time": 26500,
          "withdraw_vesting_operation_exec_time": 10400,
          "witness_set_properties_operation_exec_time": 9500,
          "witness_update_operation_exec_time": 9500,
          "claim_reward_balance2_operation_exec_time": 50300,
          "smt_setup_operation_exec_time": 41000,
          "smt_setup_emissions_operation_exec_time": 13000,
          "smt_set_setup_parameters_operation_exec_time": 40000,
          "smt_set_runtime_parameters_operation_exec_time": 39000,
          "smt_create_operation_exec_time": 50000,
          "smt_contribute_operation_exec_time": 32000,
          "smt_setup_ico_tier_operation_exec_time": 13000,
          "smt_contributor_payout_action_exec_time": 60000,
          "smt_founder_payout_action_exec_time": 69000,
          "smt_token_launch_action_exec_time": 31000,
          "smt_ico_evaluation_action_exec_time": 21000,
          "smt_ico_launch_action_exec_time": 18000,
          "smt_token_emission_action_exec_time": 2400,
          "create_proposal_operation_exec_time": 31700,
          "update_proposal_votes_operation_exec_time": 12000,
          "remove_proposal_operation_exec_time": 12000
        }
      }
    }
    

##### Example `curl`[](#rc_api.get_resource_params-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"rc_api.get_resource_params", "id":1}' https://api.hive.blog
    

* * *

*   **Since: HF20**
*   **SDK Reference**
    
    [beem](https://beem.readthedocs.io/en/latest/beem.rc.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20resource%20pool)**

#### rc\_api.get\_resource\_pool[](#rc_api.get_resource_pool)

Work in progress. See: [#2563](https://archive.ph/TlExs), [PR#2678](https://archive.ph/H0Rds)

##### Query Parameters JSON[](#rc_api.get_resource_pool-parameter_json)

    {}
    

##### Expected Response JSON[](#rc_api.get_resource_pool-expected_response_json)

    {
      "resource_pool": {
        "resource_history_bytes": {"pool": "22530662270"},
        "resource_new_accounts": {"pool": 17589594},
        "resource_market_bytes": {"pool": 1919726127},
        "resource_state_bytes": {"pool": "17720687726725"},
        "resource_execution_time": {"pool": "5835324988127"}
      }
    }
    

##### Example `curl`[](#rc_api.get_resource_pool-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"rc_api.get_resource_pool", "id":1}' https://api.hive.blog
    

* * *

*   **[Related](/search/?q=list%20rc%20accounts)**

#### rc\_api.list\_rc\_accounts[](#rc_api.list_rc_accounts)

##### Query Parameters JSON[](#rc_api.list_rc_accounts-parameter_json)

    {"start": null, "limit": 0}
    

##### Expected Response JSON[](#rc_api.list_rc_accounts-expected_response_json)

    {"rc_accounts": []}
    

* * *

*   **[Related](/search/?q=list%20rc%20direct%20delegations)**

#### rc\_api.list\_rc\_direct\_delegations[](#rc_api.list_rc_direct_delegations)

##### Query Parameters JSON[](#rc_api.list_rc_direct_delegations-parameter_json)

    {"start": null, "limit": 0}
    

##### Expected Response JSON[](#rc_api.list_rc_direct_delegations-expected_response_json)

    {"rc_direct_delegations": []}
    

* * *

### Reputation API

Methods:

*   [get\_account\_reputations](#reputation_api.get_account_reputations)

Needed by `condenser_api` to optionally use `follow_api` or `reputation_api` for account reputations (the latter if [`hivemind`](/nodeop/using-hivemind.html) is fronting `follow_api`)

*   **Since: HF20**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-account-reputations)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.account.html#beem.account.Account.get_reputation)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20account%20reputations)**

#### reputation\_api.get\_account\_reputations[](#reputation_api.get_account_reputations)

Returns the reputation of accounts. Parameters: `account:string`; `limit:int`

*   `limit` is up to 1000.

`account` (string)

`limit` (int)

 

`"hiveio"`

10

Queries the reputation for account named “hiveio”.

See [#1425](https://archive.ph/mZnIR)

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#reputation_apiget_account_reputations)

##### Query Parameters JSON[](#reputation_api.get_account_reputations-parameter_json)

    {"account_lower_bound": "", "limit": 1000}
    

##### Expected Response JSON[](#reputation_api.get_account_reputations-expected_response_json)

    {"account": "hive", "reputation": 0}
    

##### Example `curl`[](#reputation_api.get_account_reputations-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"reputation_api.get_account_reputations", "params": {"account_lower_bound": "hive"}, "id":1}' https://api.hive.blog
    

* * *

### Rewards API

Methods:

*   [simulate\_curve\_payouts](#rewards_api.simulate_curve_payouts)

Returns the simulated curve for payouts. Parameters: `curve:string`; `var1:string`

Note: **The `rewards_api` plugin is for testing purposes only, do not run in production.**

`curve` (string)

`var1` (string)

 

`"quadratic"`

“2000000000000”

 

`"bounded_curation"`

“2000000000000”

 

`"linear"`

“2000000000000”

 

`"square_root"`

“2000000000000”

 

`"convergent_linear"`

“2000000000000”

 

`"convergent_square_root"`

“2000000000000”

 

See: [#3325](https://archive.ph/ITgXq)

*   **SDK Reference**
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=simulate%20curve%20payouts)**

#### rewards\_api.simulate\_curve\_payouts[](#rewards_api.simulate_curve_payouts)

##### Query Parameters JSON[](#rewards_api.simulate_curve_payouts-parameter_json)

    {"curve": "quadratic", "var1": "2000000000000"}
    

##### Expected Response JSON[](#rewards_api.simulate_curve_payouts-expected_response_json)

    {"recent_claims": "", "payouts": []}
    

##### Example `curl`[](#rewards_api.simulate_curve_payouts-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"rewards_api.simulate_curve_payouts", "params": {"curve": "quadratic", "var1": "2000000000000"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"rewards_api.simulate_curve_payouts", "params": {"curve": "bounded_curation", "var1": "2000000000000"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"rewards_api.simulate_curve_payouts", "params": {"curve": "linear", "var1": "2000000000000"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"rewards_api.simulate_curve_payouts", "params": {"curve": "square_root", "var1": "2000000000000"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"rewards_api.simulate_curve_payouts", "params": {"curve": "convergent_linear", "var1": "2000000000000"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"rewards_api.simulate_curve_payouts", "params": {"curve": "convergent_square_root", "var1": "2000000000000"}, "id":1}' https://api.hive.blog
    

* * *

### Tags API

Methods:

*   [get\_active\_votes](#tags_api.get_active_votes)
*   [get\_comment\_discussions\_by\_payout](#tags_api.get_comment_discussions_by_payout)
*   [get\_content\_replies](#tags_api.get_content_replies)
*   [get\_discussion](#tags_api.get_discussion)
*   [get\_discussions\_by\_active](#tags_api.get_discussions_by_active)
*   [get\_discussions\_by\_author\_before\_date](#tags_api.get_discussions_by_author_before_date)
*   [get\_discussions\_by\_blog](#tags_api.get_discussions_by_blog)
*   [get\_discussions\_by\_cashout](#tags_api.get_discussions_by_cashout)
*   [get\_discussions\_by\_children](#tags_api.get_discussions_by_children)
*   [get\_discussions\_by\_comments](#tags_api.get_discussions_by_comments)
*   [get\_discussions\_by\_created](#tags_api.get_discussions_by_created)
*   [get\_discussions\_by\_feed](#tags_api.get_discussions_by_feed)
*   [get\_discussions\_by\_hot](#tags_api.get_discussions_by_hot)
*   [get\_discussions\_by\_promoted](#tags_api.get_discussions_by_promoted)
*   [get\_discussions\_by\_trending](#tags_api.get_discussions_by_trending)
*   [get\_discussions\_by\_votes](#tags_api.get_discussions_by_votes)
*   [get\_post\_discussions\_by\_payout](#tags_api.get_post_discussions_by_payout)
*   [get\_replies\_by\_last\_update](#tags_api.get_replies_by_last_update)
*   [get\_tags\_used\_by\_author](#tags_api.get_tags_used_by_author)
*   [get\_trending\_tags](#tags_api.get_trending_tags)

Used to lookup information about tags, posts, and discussions. **These AppBase API methods are still under development and subject to change.**

*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-active-votes)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-active-votes)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20active%20votes)**

#### tags\_api.get\_active\_votes[](#tags_api.get_active_votes)

**Removed since HF24** Use: [`condenser_api.get_active_votes`](/apidefinitions/#condenser_api.get_active_votes)

* * *

*   **Since: HF17**
*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-comment-discussions-by-payout)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-comment-discussions-by-payout)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20comment%20discussions%20payout)**

#### tags\_api.get\_comment\_discussions\_by\_payout[](#tags_api.get_comment_discussions_by_payout)

**Removed since HF24** Use: [`condenser_api.get_comment_discussions_by_payout`](/apidefinitions/#condenser_api.get_comment_discussions_by_payout)

* * *

*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-content-replies)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-content-replies)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20content%20replies)**

#### tags\_api.get\_content\_replies[](#tags_api.get_content_replies)

**Removed since HF24** Use: [`condenser_api.get_content_replies`](/apidefinitions/#condenser_api.get_content_replies)

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-discussions-by-trending)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.discussions.html#beem.discussions.Discussions.get_discussions)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20discussion)**

#### tags\_api.get\_discussion[](#tags_api.get_discussion)

Returns the discussion given an author and permlink.

Also see: [bridge.get\_discussion](/apidefinitions/#bridge.get_discussion)

##### Query Parameters JSON[](#tags_api.get_discussion-parameter_json)

    {"author": "", "permlink": ""}
    

##### Expected Response JSON[](#tags_api.get_discussion-expected_response_json)

    {
      "id": 0,
      "author": "",
      "permlink": "",
      "category": "",
      "parent_author": "",
      "parent_permlink": "",
      "title": "",
      "body": "",
      "json_metadata": "",
      "last_update": "1970-01-01T00:00:00",
      "created": "1970-01-01T00:00:00",
      "active": "1970-01-01T00:00:00",
      "last_payout": "1970-01-01T00:00:00",
      "depth": 0,
      "children": 0,
      "net_rshares": 0,
      "abs_rshares": 0,
      "vote_rshares": 0,
      "children_abs_rshares": 0,
      "cashout_time": "1970-01-01T00:00:00",
      "max_cashout_time": "1970-01-01T00:00:00",
      "total_vote_weight": 0,
      "reward_weight": 0,
      "total_payout_value": {
        "amount": "0",
        "precision": 3,
        "nai": "@@000000021"
      },
      "curator_payout_value": {
        "amount": "0",
        "precision": 3,
        "nai": "@@000000021"
      },
      "author_rewards": 0,
      "net_votes": 0,
      "root_author": "",
      "root_permlink": "",
      "max_accepted_payout": {
        "amount": "0",
        "precision": 3,
        "nai": "@@000000021"
      },
      "percent_hbd": 0,
      "allow_replies": false,
      "allow_votes": false,
      "allow_curation_rewards": false,
      "beneficiaries": [],
      "url": "",
      "root_title": "",
      "pending_payout_value": {
        "amount": "0",
        "precision": 3,
        "nai": "@@000000021"
      },
      "total_pending_payout_value": {
        "amount": "0",
        "precision": 3,
        "nai": "@@000000021"
      },
      "active_votes": [],
      "replies": [],
      "author_reputation": 0,
      "promoted": {
        "amount": "0",
        "precision": 3,
        "nai": "@@000000013"
      },
      "body_length": 0,
      "reblogged_by": []
    }
    

##### Example `curl`[](#tags_api.get_discussion-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"tags_api.get_discussion", "params":{"author":"hiveio", "permlink":"firstpost"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"tags_api.get_discussion", "params":{"author":"alice", "permlink":"a-post-by-alice"}, "id":1}' https://api.hive.blog
    

* * *

*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-discussions-by-active)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-discussions-by-active)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20discussions%20active)**

#### tags\_api.get\_discussions\_by\_active[](#tags_api.get_discussions_by_active)

**Removed since HF24** Use: [`condenser_api.get_discussions_by_active`](/apidefinitions/#condenser_api.get_discussions_by_active)

* * *

*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-discussions-by-author-before-date)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-discussions-by-author-before-date)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20discussions%20author%20date)**

#### tags\_api.get\_discussions\_by\_author\_before\_date[](#tags_api.get_discussions_by_author_before_date)

**Removed since HF24** Use: [`condenser_api.get_discussions_by_author_before_date`](/apidefinitions/#condenser_api.get_discussions_by_author_before_date)

Also see: [Paginated API Methods](/tutorials-recipes/paginated-api-methods.html#tags_apiget_discussions_by_author_before_date)

* * *

*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-discussions-by-blog)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-discussions-by-blog)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20discussions%20blog)**

#### tags\_api.get\_discussions\_by\_blog[](#tags_api.get_discussions_by_blog)

**Removed since HF24** Use: [`condenser_api.get_discussions_by_blog`](/apidefinitions/#condenser_api.get_discussions_by_blog)

* * *

*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-discussions-by-cashout)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-discussions-by-cashout)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20discussions%20cashout)**

#### tags\_api.get\_discussions\_by\_cashout[](#tags_api.get_discussions_by_cashout)

**Removed since HF24** Use: [`condenser_api.get_discussions_by_cashout`](/apidefinitions/#condenser_api.get_discussions_by_cashout)

* * *

*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-discussions-by-children)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-discussions-by-children)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20discussions%20children)**

#### tags\_api.get\_discussions\_by\_children[](#tags_api.get_discussions_by_children)

**Removed since HF24** Use: [`condenser_api.get_discussions_by_children`](/apidefinitions/#condenser_api.get_discussions_by_children)

Returns a list of discussions by children.

* * *

*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-discussions-by-comments)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-discussions-by-comments)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20discussions%20comments)**

#### tags\_api.get\_discussions\_by\_comments[](#tags_api.get_discussions_by_comments)

**Removed since HF24** Use: [`condenser_api.get_discussions_by_comments`](/apidefinitions/#condenser_api.get_discussions_by_comments)

* * *

*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-discussions-by-created)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-discussions-by-created)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20discussions%20created)**

#### tags\_api.get\_discussions\_by\_created[](#tags_api.get_discussions_by_created)

**Removed since HF24** Use: [`condenser_api.get_discussions_by_created`](/apidefinitions/#condenser_api.get_discussions_by_created)

* * *

*   **Since: HF14**
*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-discussions-by-feed)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-discussions-by-feed)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20discussions%20feed)**

#### tags\_api.get\_discussions\_by\_feed[](#tags_api.get_discussions_by_feed)

**Removed since HF24** Use: [`condenser_api.get_discussions_by_feed`](/apidefinitions/#condenser_api.get_discussions_by_feed)

* * *

*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-discussions-by-hot)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-discussions-by-hot)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20discussions%20hot)**

#### tags\_api.get\_discussions\_by\_hot[](#tags_api.get_discussions_by_hot)

**Removed since HF24** Use: [`condenser_api.get_discussions_by_hot`](/apidefinitions/#condenser_api.get_discussions_by_hot)

* * *

*   **Since: HF13**
*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-discussions-by-promoted)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-discussions-by-promoted)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20discussions%20promoted)**

#### tags\_api.get\_discussions\_by\_promoted[](#tags_api.get_discussions_by_promoted)

**Removed since HF24** Use: [`condenser_api.get_discussions_by_promoted`](/apidefinitions/#condenser_api.get_discussions_by_promoted)

* * *

*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-discussions-by-trending)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-discussions-by-trending)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20discussions%20trending)**

#### tags\_api.get\_discussions\_by\_trending[](#tags_api.get_discussions_by_trending)

**Removed since HF24** Use: [`condenser_api.get_discussions_by_trending`](/apidefinitions/#condenser_api.get_discussions_by_trending)

* * *

*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-discussions-by-votes)
    
    [beem](https://beem.readthedocs.io/en/latest/apidefinitions.html#get-discussions-by-votes)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20discussions%20votes)**

#### tags\_api.get\_discussions\_by\_votes[](#tags_api.get_discussions_by_votes)

**Removed since HF24** Use: [`condenser_api.get_discussions_by_votes`](/apidefinitions/#condenser_api.get_discussions_by_votes)

* * *

*   **Since: HF17**
*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-discussions-by-payout)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.discussions.html#beem.discussions.Post_discussions_by_payout)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20post%20discussions%20payout)**

#### tags\_api.get\_post\_discussions\_by\_payout[](#tags_api.get_post_discussions_by_payout)

**Removed since HF24** Use: [`condenser_api.get_post_discussions_by_payout`](/apidefinitions/#condenser_api.get_post_discussions_by_payout)

* * *

*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#content)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.discussions.html#beem.discussions.Replies_by_last_update)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20replies%20last%20update)**

#### tags\_api.get\_replies\_by\_last\_update[](#tags_api.get_replies_by_last_update)

**Removed since HF24** Use: [`condenser_api.get_replies_by_last_update`](/apidefinitions/#condenser_api.get_replies_by_last_update)

* * *

*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#tags)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.account.html#beem.account.Account.get_tags_used_by_author)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20tags%20used%20author)**

#### tags\_api.get\_tags\_used\_by\_author[](#tags_api.get_tags_used_by_author)

**Removed since HF24** Use: [`condenser_api.get_tags_used_by_author`](/apidefinitions/#condenser_api.get_tags_used_by_author)

* * *

*   **Removed**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-trending-tags)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.discussions.html#beem.discussions.Trending_tags)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20trending%20tags)**

#### tags\_api.get\_trending\_tags[](#tags_api.get_trending_tags)

**Removed since HF24** Use: [`condenser_api.get_trending_tags`](/apidefinitions/#condenser_api.get_trending_tags)

* * *

### Transaction Status API

Methods:

*   [find\_transaction](#transaction_status_api.find_transaction)

This API is intended to evaluate a transaction status after calling [`condenser_api.broadcast_transaction`](/apidefinitions/#condenser_api.broadcast_transaction).

To enable this API for `hived`, the following is required in `config.ini` by specifying:

    plugin = transaction_status_api
    

See: [#3060](https://archive.ph/He9N1)

*   **Since: HF23**
*   **SDK Reference**
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=find%20transaction)**

#### transaction\_status\_api.find\_transaction[](#transaction_status_api.find_transaction)

Returns the status of a given transaction id. Parameters: `trx_id:string`; `expiration:timestamp` (optional)

The result will contain one of the following `status` values:

Status

Meaning

`unknown`

Expiration time in future, transaction not included in block or mempool

`within_mempool`

Transaction in mempool

`within_reversible_block`

Transaction has been included in block, block not irreversible

`within_irreversible_block`

Transaction has been included in block, block is irreversible

`expired_reversible`

Transaction has expired, transaction is not irreversible (transaction could be in a fork)

`expired_irreversible`

Transaction has expired, transaction is irreversible (transaction cannot be in a fork)

`too_old`

Transaction is too old, I don’t know about it

##### Query Parameters JSON[](#transaction_status_api.find_transaction-parameter_json)

    {
      "transaction_id": "0000000000000000000000000000000000000000",
      "expiration": "2016-03-24T18:00:21"
    }
    

##### Expected Response JSON[](#transaction_status_api.find_transaction-expected_response_json)

    {"status": "unknown"}
    

##### Example `curl`[](#transaction_status_api.find_transaction-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"transaction_status_api.find_transaction", "params": {"transaction_id": "0000000000000000000000000000000000000000"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"transaction_status_api.find_transaction", "params": {"transaction_id": "0000000000000000000000000000000000000000", "expiration":"2016-03-24T18:00:21"}, "id":1}' https://api.hive.blog
    

* * *

### Wallet Bridge API

Methods:

*   [broadcast\_transaction](#wallet_bridge_api.broadcast_transaction)
*   [broadcast\_transaction\_synchronous](#wallet_bridge_api.broadcast_transaction_synchronous)
*   [find\_proposals](#wallet_bridge_api.find_proposals)
*   [find\_rc\_accounts](#wallet_bridge_api.find_rc_accounts)
*   [find\_recurrent\_transfers](#wallet_bridge_api.find_recurrent_transfers)
*   [get\_account](#wallet_bridge_api.get_account)
*   [get\_account\_history](#wallet_bridge_api.get_account_history)
*   [get\_accounts](#wallet_bridge_api.get_accounts)
*   [get\_active\_witnesses](#wallet_bridge_api.get_active_witnesses)
*   [get\_block](#wallet_bridge_api.get_block)
*   [get\_chain\_properties](#wallet_bridge_api.get_chain_properties)
*   [get\_collateralized\_conversion\_requests](#wallet_bridge_api.get_collateralized_conversion_requests)
*   [get\_conversion\_requests](#wallet_bridge_api.get_conversion_requests)
*   [get\_current\_median\_history\_price](#wallet_bridge_api.get_current_median_history_price)
*   [get\_dynamic\_global\_properties](#wallet_bridge_api.get_dynamic_global_properties)
*   [get\_feed\_history](#wallet_bridge_api.get_feed_history)
*   [get\_hardfork\_version](#wallet_bridge_api.get_hardfork_version)
*   [get\_open\_orders](#wallet_bridge_api.get_open_orders)
*   [get\_ops\_in\_block](#wallet_bridge_api.get_ops_in_block)
*   [get\_order\_book](#wallet_bridge_api.get_order_book)
*   [get\_owner\_history](#wallet_bridge_api.get_owner_history)
*   [get\_reward\_fund](#wallet_bridge_api.get_reward_fund)
*   [get\_transaction](#wallet_bridge_api.get_transaction)
*   [get\_version](#wallet_bridge_api.get_version)
*   [get\_withdraw\_routes](#wallet_bridge_api.get_withdraw_routes)
*   [get\_witness](#wallet_bridge_api.get_witness)
*   [get\_witness\_schedule](#wallet_bridge_api.get_witness_schedule)
*   [is\_known\_transaction](#wallet_bridge_api.is_known_transaction)
*   [list\_accounts](#wallet_bridge_api.list_accounts)
*   [list\_my\_accounts](#wallet_bridge_api.list_my_accounts)
*   [list\_proposal\_votes](#wallet_bridge_api.list_proposal_votes)
*   [list\_proposals](#wallet_bridge_api.list_proposals)
*   [list\_rc\_accounts](#wallet_bridge_api.list_rc_accounts)
*   [list\_rc\_direct\_delegations](#wallet_bridge_api.list_rc_direct_delegations)
*   [list\_witnesses](#wallet_bridge_api.list_witnesses)

Required for `cli_wallet` interactions. Remember that you need to add `plugin = wallet_bridge_api` in your `config.ini` file if you are going to use `cli_wallet`.

See: [Hive HardFork 26 Jump Starter Kit](https://hive.blog/hive-160391/@gtg/hive-hardfork-26-jump-starter-kit)

*   **Since: HF26**
*   **[Related](/search/?q=broadcast%20transaction)**

#### wallet\_bridge\_api.broadcast\_transaction[](#wallet_bridge_api.broadcast_transaction)

##### Query Parameters JSON[](#wallet_bridge_api.broadcast_transaction-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.broadcast_transaction-expected_response_json)

    {}
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=broadcast%20transaction%20synchronous)**

#### wallet\_bridge\_api.broadcast\_transaction\_synchronous[](#wallet_bridge_api.broadcast_transaction_synchronous)

##### Query Parameters JSON[](#wallet_bridge_api.broadcast_transaction_synchronous-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.broadcast_transaction_synchronous-expected_response_json)

    {
      "id": "0000000000000000000000000000000000000000",
      "block_num": 0,
      "trx_num": 0,
      "expired": false
    }
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=find%20proposals)**

#### wallet\_bridge\_api.find\_proposals[](#wallet_bridge_api.find_proposals)

##### Query Parameters JSON[](#wallet_bridge_api.find_proposals-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.find_proposals-expected_response_json)

    {"proposals": []}
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=find%20rc%20accounts)**

#### wallet\_bridge\_api.find\_rc\_accounts[](#wallet_bridge_api.find_rc_accounts)

##### Query Parameters JSON[](#wallet_bridge_api.find_rc_accounts-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.find_rc_accounts-expected_response_json)

    []
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=find%20recurrent%20transfers)**

#### wallet\_bridge\_api.find\_recurrent\_transfers[](#wallet_bridge_api.find_recurrent_transfers)

##### Query Parameters JSON[](#wallet_bridge_api.find_recurrent_transfers-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.find_recurrent_transfers-expected_response_json)

    []
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=get%20account)**

#### wallet\_bridge\_api.get\_account[](#wallet_bridge_api.get_account)

##### Query Parameters JSON[](#wallet_bridge_api.get_account-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.get_account-expected_response_json)

    null
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=get%20account%20history)**

#### wallet\_bridge\_api.get\_account\_history[](#wallet_bridge_api.get_account_history)

##### Query Parameters JSON[](#wallet_bridge_api.get_account_history-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.get_account_history-expected_response_json)

    []
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=get%20accounts)**

#### wallet\_bridge\_api.get\_accounts[](#wallet_bridge_api.get_accounts)

##### Query Parameters JSON[](#wallet_bridge_api.get_accounts-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.get_accounts-expected_response_json)

    []
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=get%20active%20witnesses)**

#### wallet\_bridge\_api.get\_active\_witnesses[](#wallet_bridge_api.get_active_witnesses)

##### Query Parameters JSON[](#wallet_bridge_api.get_active_witnesses-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.get_active_witnesses-expected_response_json)

    {"witnesses": []}
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=get%20block)**

#### wallet\_bridge\_api.get\_block[](#wallet_bridge_api.get_block)

##### Query Parameters JSON[](#wallet_bridge_api.get_block-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.get_block-expected_response_json)

    {}
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=get%20chain%20properties)**

#### wallet\_bridge\_api.get\_chain\_properties[](#wallet_bridge_api.get_chain_properties)

##### Query Parameters JSON[](#wallet_bridge_api.get_chain_properties-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.get_chain_properties-expected_response_json)

    {
      "account_creation_fee": {
        "amount": "1",
        "precision": 3,
        "nai": "@@000000021"
      },
      "maximum_block_size": 131072,
      "hbd_interest_rate": 1000,
      "account_subsidy_budget": 797,
      "account_subsidy_decay": 347321
    }
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=get%20collateralized%20conversion%20requests)**

#### wallet\_bridge\_api.get\_collateralized\_conversion\_requests[](#wallet_bridge_api.get_collateralized_conversion_requests)

##### Query Parameters JSON[](#wallet_bridge_api.get_collateralized_conversion_requests-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.get_collateralized_conversion_requests-expected_response_json)

    []
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=get%20conversion%20requests)**

#### wallet\_bridge\_api.get\_conversion\_requests[](#wallet_bridge_api.get_conversion_requests)

##### Query Parameters JSON[](#wallet_bridge_api.get_conversion_requests-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.get_conversion_requests-expected_response_json)

    []
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=get%20current%20median%20history%20price)**

#### wallet\_bridge\_api.get\_current\_median\_history\_price[](#wallet_bridge_api.get_current_median_history_price)

##### Query Parameters JSON[](#wallet_bridge_api.get_current_median_history_price-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.get_current_median_history_price-expected_response_json)

    {
      "base": {
        "amount": "0",
        "precision": 3,
        "nai": "@@000000021"
      },
      "quote": {
        "amount": "0",
        "precision": 3,
        "nai": "@@000000021"
      }
    }
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=get%20dynamic%20global%20properties)**

#### wallet\_bridge\_api.get\_dynamic\_global\_properties[](#wallet_bridge_api.get_dynamic_global_properties)

##### Query Parameters JSON[](#wallet_bridge_api.get_dynamic_global_properties-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.get_dynamic_global_properties-expected_response_json)

    {
      "id": 0,
      "head_block_number": 0,
      "head_block_id": "0000000000000000000000000000000000000000",
      "time": "1970-01-01T00:00:00",
      "current_witness": "",
      "total_pow": 0,
      "num_pow_witnesses": 0,
      "virtual_supply": {
        "amount": "0",
        "precision": 3,
        "nai": "@@000000021"
      },
      "current_supply": {
        "amount": "0",
        "precision": 3,
        "nai": "@@000000021"
      },
      "init_hbd_supply": {
        "amount": "0",
        "precision": 3,
        "nai": "@@000000021"
      },
      "current_hbd_supply": {
        "amount": "0",
        "precision": 3,
        "nai": "@@000000021"
      },
      "total_vesting_fund_hive": {
        "amount": "0",
        "precision": 3,
        "nai": "@@000000021"
      },
      "total_vesting_shares": {
        "amount": "0",
        "precision": 3,
        "nai": "@@000000021"
      },
      "total_reward_fund_hive": {
        "amount": "0",
        "precision": 3,
        "nai": "@@000000021"
      },
      "total_reward_shares2": "0",
      "pending_rewarded_vesting_shares": {
        "amount": "0",
        "precision": 3,
        "nai": "@@000000021"
      },
      "pending_rewarded_vesting_hive": {
        "amount": "0",
        "precision": 3,
        "nai": "@@000000021"
      },
      "hbd_interest_rate": 0,
      "hbd_print_rate": 0,
      "maximum_block_size": 0,
      "required_actions_partition_percent": 0,
      "current_aslot": 0,
      "recent_slots_filled": "0",
      "participation_count": 0,
      "last_irreversible_block_num": 0,
      "vote_power_reserve_rate": 0,
      "delegation_return_period": 0,
      "reverse_auction_seconds": 0,
      "available_account_subsidies": 0,
      "hbd_stop_percent": 0,
      "hbd_start_percent": 0,
      "next_maintenance_time": "1970-01-01T00:00:00",
      "last_budget_time": "1970-01-01T00:00:00",
      "next_daily_maintenance_time": "1970-01-01T00:00:00",
      "content_reward_percent": 0,
      "vesting_reward_percent": 0,
      "proposal_fund_percent": 0,
      "dhf_interval_ledger": {
        "amount": "0",
        "precision": 3,
        "nai": "@@000000021"
      },
      "downvote_pool_percent": 0,
      "current_remove_threshold": 0,
      "early_voting_seconds": 0,
      "mid_voting_seconds": 0,
      "max_consecutive_recurrent_transfer_failures": 10,
      "max_recurrent_transfer_end_date": 730,
      "min_recurrent_transfers_recurrence": 24,
      "max_open_recurrent_transfers": 255
    }
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=get%20feed%20history)**

#### wallet\_bridge\_api.get\_feed\_history[](#wallet_bridge_api.get_feed_history)

##### Query Parameters JSON[](#wallet_bridge_api.get_feed_history-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.get_feed_history-expected_response_json)

    {
      "id": 0,
      "current_median_history": {
        "base": {
          "amount": "0",
          "precision": 3,
          "nai": "@@000000021"
        },
        "quote": {
          "amount": "0",
          "precision": 3,
          "nai": "@@000000021"
        }
      },
      "market_median_history": {
        "base": {
          "amount": "0",
          "precision": 3,
          "nai": "@@000000021"
        },
        "quote": {
          "amount": "0",
          "precision": 3,
          "nai": "@@000000021"
        }
      },
      "current_min_history": {
        "base": {
          "amount": "0",
          "precision": 3,
          "nai": "@@000000021"
        },
        "quote": {
          "amount": "0",
          "precision": 3,
          "nai": "@@000000021"
        }
      },
      "current_max_history": {
        "base": {
          "amount": "0",
          "precision": 3,
          "nai": "@@000000021"
        },
        "quote": {
          "amount": "0",
          "precision": 3,
          "nai": "@@000000021"
        }
      },
      "price_history": []
    }
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=get%20hardfork%20version)**

#### wallet\_bridge\_api.get\_hardfork\_version[](#wallet_bridge_api.get_hardfork_version)

##### Query Parameters JSON[](#wallet_bridge_api.get_hardfork_version-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.get_hardfork_version-expected_response_json)

    "0.0.0"
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=get%20open%20orders)**

#### wallet\_bridge\_api.get\_open\_orders[](#wallet_bridge_api.get_open_orders)

##### Query Parameters JSON[](#wallet_bridge_api.get_open_orders-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.get_open_orders-expected_response_json)

    []
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=get%20ops%20block)**

#### wallet\_bridge\_api.get\_ops\_in\_block[](#wallet_bridge_api.get_ops_in_block)

##### Query Parameters JSON[](#wallet_bridge_api.get_ops_in_block-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.get_ops_in_block-expected_response_json)

    {"ops": []}
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=get%20order%20book)**

#### wallet\_bridge\_api.get\_order\_book[](#wallet_bridge_api.get_order_book)

##### Query Parameters JSON[](#wallet_bridge_api.get_order_book-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.get_order_book-expected_response_json)

    {"bids": [], "asks": []}
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=get%20owner%20history)**

#### wallet\_bridge\_api.get\_owner\_history[](#wallet_bridge_api.get_owner_history)

##### Query Parameters JSON[](#wallet_bridge_api.get_owner_history-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.get_owner_history-expected_response_json)

    {"owner_auths": []}
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=get%20reward%20fund)**

#### wallet\_bridge\_api.get\_reward\_fund[](#wallet_bridge_api.get_reward_fund)

##### Query Parameters JSON[](#wallet_bridge_api.get_reward_fund-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.get_reward_fund-expected_response_json)

    {
      "id": 0,
      "name": "",
      "reward_balance": {
        "amount": "0",
        "precision": 3,
        "nai": "@@000000021"
      },
      "recent_claims": "0",
      "last_update": "1970-01-01T00:00:00",
      "content_constant": "0",
      "percent_curation_rewards": 0,
      "percent_content_rewards": 0,
      "author_reward_curve": "quadratic",
      "curation_reward_curve": "quadratic"
    }
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=get%20transaction)**

#### wallet\_bridge\_api.get\_transaction[](#wallet_bridge_api.get_transaction)

##### Query Parameters JSON[](#wallet_bridge_api.get_transaction-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.get_transaction-expected_response_json)

    {
      "ref_block_num": 0,
      "ref_block_prefix": 0,
      "expiration": "1970-01-01T00:00:00",
      "operations": [],
      "extensions": [],
      "signatures": [],
      "transaction_id": "0000000000000000000000000000000000000000",
      "block_num": 0,
      "transaction_num": 0
    }
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=get%20version)**

#### wallet\_bridge\_api.get\_version[](#wallet_bridge_api.get_version)

##### Query Parameters JSON[](#wallet_bridge_api.get_version-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.get_version-expected_response_json)

    {}
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=get%20withdraw%20routes)**

#### wallet\_bridge\_api.get\_withdraw\_routes[](#wallet_bridge_api.get_withdraw_routes)

##### Query Parameters JSON[](#wallet_bridge_api.get_withdraw_routes-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.get_withdraw_routes-expected_response_json)

    []
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=get%20witness)**

#### wallet\_bridge\_api.get\_witness[](#wallet_bridge_api.get_witness)

##### Query Parameters JSON[](#wallet_bridge_api.get_witness-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.get_witness-expected_response_json)

    null
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=get%20witness%20schedule)**

#### wallet\_bridge\_api.get\_witness\_schedule[](#wallet_bridge_api.get_witness_schedule)

##### Query Parameters JSON[](#wallet_bridge_api.get_witness_schedule-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.get_witness_schedule-expected_response_json)

    {
      "id": 0,
      "current_virtual_time": "0",
      "next_shuffle_block_num": 944743200,
      "current_shuffled_witnesses": [],
      "num_scheduled_witnesses": 8,
      "elected_weight": 226,
      "timeshare_weight": 142,
      "miner_weight": 10,
      "witness_pay_normalization_factor": 32765,
      "median_props": {
        "account_creation_fee": {
          "amount": "1",
          "precision": 3,
          "nai": "@@000000021"
        },
        "maximum_block_size": 131072,
        "hbd_interest_rate": 1000,
        "account_subsidy_budget": 797,
        "account_subsidy_decay": 347321
      },
      "majority_version": "0.0.0",
      "max_voted_witnesses": 32,
      "max_miner_witnesses": 41,
      "max_runner_witnesses": 203,
      "hardfork_required_witnesses": 52,
      "account_subsidy_rd": {
        "resource_unit": 0,
        "budget_per_time_unit": 0,
        "pool_eq": 0,
        "max_pool_size": 0,
        "decay_params": {
          "decay_per_time_unit": 0,
          "decay_per_time_unit_denom_shift": 0
        },
        "min_decay": 0
      },
      "account_subsidy_witness_rd": {
        "resource_unit": 0,
        "budget_per_time_unit": 0,
        "pool_eq": 0,
        "max_pool_size": 0,
        "decay_params": {
          "decay_per_time_unit": 0,
          "decay_per_time_unit_denom_shift": 0
        },
        "min_decay": 0
      },
      "min_witness_account_subsidy_decay": 0
    }
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=known%20transaction)**

#### wallet\_bridge\_api.is\_known\_transaction[](#wallet_bridge_api.is_known_transaction)

##### Query Parameters JSON[](#wallet_bridge_api.is_known_transaction-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.is_known_transaction-expected_response_json)

    false
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=list%20accounts)**

#### wallet\_bridge\_api.list\_accounts[](#wallet_bridge_api.list_accounts)

##### Query Parameters JSON[](#wallet_bridge_api.list_accounts-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.list_accounts-expected_response_json)

    []
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=list%20accounts)**

#### wallet\_bridge\_api.list\_my\_accounts[](#wallet_bridge_api.list_my_accounts)

##### Query Parameters JSON[](#wallet_bridge_api.list_my_accounts-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.list_my_accounts-expected_response_json)

    []
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=list%20proposal%20votes)**

#### wallet\_bridge\_api.list\_proposal\_votes[](#wallet_bridge_api.list_proposal_votes)

##### Query Parameters JSON[](#wallet_bridge_api.list_proposal_votes-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.list_proposal_votes-expected_response_json)

    {"proposal_votes": []}
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=list%20proposals)**

#### wallet\_bridge\_api.list\_proposals[](#wallet_bridge_api.list_proposals)

##### Query Parameters JSON[](#wallet_bridge_api.list_proposals-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.list_proposals-expected_response_json)

    {"proposals": []}
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=list%20rc%20accounts)**

#### wallet\_bridge\_api.list\_rc\_accounts[](#wallet_bridge_api.list_rc_accounts)

##### Query Parameters JSON[](#wallet_bridge_api.list_rc_accounts-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.list_rc_accounts-expected_response_json)

    []
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=list%20rc%20direct%20delegations)**

#### wallet\_bridge\_api.list\_rc\_direct\_delegations[](#wallet_bridge_api.list_rc_direct_delegations)

##### Query Parameters JSON[](#wallet_bridge_api.list_rc_direct_delegations-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.list_rc_direct_delegations-expected_response_json)

    []
    

* * *

*   **Since: HF26**
*   **[Related](/search/?q=list%20witnesses)**

#### wallet\_bridge\_api.list\_witnesses[](#wallet_bridge_api.list_witnesses)

##### Query Parameters JSON[](#wallet_bridge_api.list_witnesses-parameter_json)

    null
    

##### Expected Response JSON[](#wallet_bridge_api.list_witnesses-expected_response_json)

    {"witnesses": []}
    

* * *

### Witness API

Methods:

*   [get\_account\_bandwidth](#witness_api.get_account_bandwidth)
*   [get\_reserve\_ratio](#witness_api.get_reserve_ratio)

**API removed in 0.20.6, see: [#3029](https://archive.ph/eeEeq#issuecomment-428404844)**

*   **Disabled**
*   **[Related](/search/?q=get%20account%20bandwidth)**

#### witness\_api.get\_account\_bandwidth[](#witness_api.get_account_bandwidth)

**Disabled since 0.20.6, see: [#3029](https://archive.ph/eeEeq#issuecomment-428404844)**

Returns the available bandwidth of an account. See: [Forum/Market Bandwidth](/tutorials-recipes/forum-market-bandwidth.html)

##### Query Parameters JSON[](#witness_api.get_account_bandwidth-parameter_json)

    {"account": "", "type": "post"}
    

##### Expected Response JSON[](#witness_api.get_account_bandwidth-expected_response_json)

    {}
    

* * *

*   **Disabled**
*   **SDK Reference**
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Api)
    
*   **[Related](/search/?q=get%20reserve%20ratio)**

#### witness\_api.get\_reserve\_ratio[](#witness_api.get_reserve_ratio)

**Disabled since 0.20.6, see: [#3029](https://archive.ph/eeEeq#issuecomment-428404844)**

Returns the current reserve ratio.

##### Query Parameters JSON[](#witness_api.get_reserve_ratio-parameter_json)

    {}
    

##### Expected Response JSON[](#witness_api.get_reserve_ratio-expected_response_json)

    {
      "id": 0,
      "average_block_size": 0,
      "current_reserve_ratio": 1,
      "max_virtual_bandwidth": "0"
    }
    

##### Example `curl`[](#witness_api.get_reserve_ratio-curl-examples)

    curl -s --data '{"jsonrpc":"2.0", "method":"witness_api.get_account_bandwidth", "params":{"account":"hiveio","type":"forum"}, "id":1}' https://api.hive.blog
    

    curl -s --data '{"jsonrpc":"2.0", "method":"witness_api.get_account_bandwidth", "params":{"account":"alice","type":"market"}, "id":1}' https://api.hive.blog
    

* * *

### Broadcast OPS

Ops:

*   [account\_create](#broadcast_ops_account_create)
*   [account\_create\_with\_delegation](#broadcast_ops_account_create_with_delegation)
*   [account\_update](#broadcast_ops_account_update)
*   [account\_update2](#broadcast_ops_account_update2)
*   [account\_witness\_proxy](#broadcast_ops_account_witness_proxy)
*   [account\_witness\_vote](#broadcast_ops_account_witness_vote)
*   [cancel\_transfer\_from\_savings](#broadcast_ops_cancel_transfer_from_savings)
*   [change\_recovery\_account](#broadcast_ops_change_recovery_account)
*   [claim\_account](#broadcast_ops_claim_account)
*   [claim\_reward\_balance](#broadcast_ops_claim_reward_balance)
*   [claim\_reward\_balance2](#broadcast_ops_claim_reward_balance2)
*   [collateralized\_convert](#broadcast_ops_collateralized_convert)
*   [comment](#broadcast_ops_comment)
*   [comment\_options](#broadcast_ops_comment_options)
*   [convert](#broadcast_ops_convert)
*   [create\_claimed\_account](#broadcast_ops_create_claimed_account)
*   [create\_proposal](#broadcast_ops_create_proposal)
*   [custom](#broadcast_ops_custom)
*   [custom\_binary](#broadcast_ops_custom_binary)
*   [custom\_json](#broadcast_ops_custom_json)
*   [decline\_voting\_rights](#broadcast_ops_decline_voting_rights)
*   [delegate\_vesting\_shares](#broadcast_ops_delegate_vesting_shares)
*   [delete\_comment](#broadcast_ops_delete_comment)
*   [escrow\_approve](#broadcast_ops_escrow_approve)
*   [escrow\_dispute](#broadcast_ops_escrow_dispute)
*   [escrow\_release](#broadcast_ops_escrow_release)
*   [escrow\_transfer](#broadcast_ops_escrow_transfer)
*   [feed\_publish](#broadcast_ops_feed_publish)
*   [limit\_order\_cancel](#broadcast_ops_limit_order_cancel)
*   [limit\_order\_create](#broadcast_ops_limit_order_create)
*   [limit\_order\_create2](#broadcast_ops_limit_order_create2)
*   [pow](#broadcast_ops_pow)
*   [pow2](#broadcast_ops_pow2)
*   [price](#broadcast_ops_price)
*   [prove\_authority](#broadcast_ops_prove_authority)
*   [recover\_account](#broadcast_ops_recover_account)
*   [recurrent\_transfer](#broadcast_ops_recurrent_transfer)
*   [remove\_proposal](#broadcast_ops_remove_proposal)
*   [request\_account\_recovery](#broadcast_ops_request_account_recovery)
*   [set\_withdraw\_vesting\_route](#broadcast_ops_set_withdraw_vesting_route)
*   [smt\_contribute](#broadcast_ops_smt_contribute)
*   [smt\_create](#broadcast_ops_smt_create)
*   [smt\_set\_runtime\_parameters](#broadcast_ops_smt_set_runtime_parameters)
*   [smt\_set\_setup\_parameters](#broadcast_ops_smt_set_setup_parameters)
*   [smt\_setup](#broadcast_ops_smt_setup)
*   [smt\_setup\_emissions](#broadcast_ops_smt_setup_emissions)
*   [transfer](#broadcast_ops_transfer)
*   [transfer\_from\_savings](#broadcast_ops_transfer_from_savings)
*   [transfer\_to\_savings](#broadcast_ops_transfer_to_savings)
*   [transfer\_to\_vesting](#broadcast_ops_transfer_to_vesting)
*   [update\_proposal](#broadcast_ops_update_proposal)
*   [update\_proposal\_votes](#broadcast_ops_update_proposal_votes)
*   [vote](#broadcast_ops_vote)
*   [vote2](#broadcast_ops_vote2)
*   [withdraw\_vesting](#broadcast_ops_withdraw_vesting)
*   [witness\_block\_approve](#broadcast_ops_witness_block_approve)
*   [witness\_set\_properties](#broadcast_ops_witness_set_properties)
*   [witness\_update](#broadcast_ops_witness_update)

Virtual Ops:

*   [account\_created](#broadcast_ops_account_created)
*   [author\_reward](#broadcast_ops_author_reward)
*   [changed\_recovery\_account](#broadcast_ops_changed_recovery_account)
*   [clear\_null\_account\_balance](#broadcast_ops_clear_null_account_balance)
*   [comment\_benefactor\_reward](#broadcast_ops_comment_benefactor_reward)
*   [comment\_payout\_update](#broadcast_ops_comment_payout_update)
*   [comment\_reward](#broadcast_ops_comment_reward)
*   [consolidate\_treasury\_balance](#broadcast_ops_consolidate_treasury_balance)
*   [curation\_reward](#broadcast_ops_curation_reward)
*   [delayed\_voting](#broadcast_ops_delayed_voting)
*   [effective\_comment\_vote](#broadcast_ops_effective_comment_vote)
*   [expired\_account\_notification](#broadcast_ops_expired_account_notification)
*   [failed\_recurrent\_transfer](#broadcast_ops_failed_recurrent_transfer)
*   [fill\_collateralized\_convert\_request](#broadcast_ops_fill_collateralized_convert_request)
*   [fill\_convert\_request](#broadcast_ops_fill_convert_request)
*   [fill\_order](#broadcast_ops_fill_order)
*   [fill\_recurrent\_transfer](#broadcast_ops_fill_recurrent_transfer)
*   [fill\_transfer\_from\_savings](#broadcast_ops_fill_transfer_from_savings)
*   [fill\_vesting\_withdraw](#broadcast_ops_fill_vesting_withdraw)
*   [hardfork](#broadcast_ops_hardfork)
*   [hardfork\_hive](#broadcast_ops_hardfork_hive)
*   [hardfork\_hive\_restore](#broadcast_ops_hardfork_hive_restore)
*   [ineffective\_delete\_comment](#broadcast_ops_ineffective_delete_comment)
*   [interest](#broadcast_ops_interest)
*   [producer\_reward](#broadcast_ops_producer_reward)
*   [proposal\_pay](#broadcast_ops_proposal_pay)
*   [return\_vesting\_delegation](#broadcast_ops_return_vesting_delegation)
*   [shutdown\_witness](#broadcast_ops_shutdown_witness)
*   [sps\_convert](#broadcast_ops_sps_convert)
*   [sps\_fund](#broadcast_ops_sps_fund)
*   [transfer\_to\_vesting\_completed](#broadcast_ops_transfer_to_vesting_completed)

An operation on Hive is a way of expressing intention on the blockchain. They are also known as Broadcast Operations. They have types, like `vote` or `comment`. They pass parameters like `author` and `permlink`, depending on what their purpose is.

Operations are grouped into transactions and passed as parameters to methods like `network_broadcast_api.broadcast_transaction`, in the `operations` array. Transactions must be signed in order for the blockchain to accept them. Here is an example of a transaction that contains one operation (shown without signatures).

    {
       "jsonrpc":"2.0",
       "method":"condenser_api.broadcast_transaction",
       "params":{
          "trx":{
             "ref_block_num":1097,
             "ref_block_prefix":2181793527,
             "expiration":"2016-03-24T18:00:21",
             "operations":[
                [
                   "vote",
                   {
                      "voter":"hiveio",
                      "author":"alice",
                      "permlink":"a-post-by-alice",
                      "weight":10000
                   }
                ]
             ],
             "extensions":[],
             "signatures":[]
          }
       },
       "id":1
    }
    

Also see: [Broadcast Transaction](/apidefinitions/#condenser_api.broadcast_transaction)

*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/00_vote.md)
    
    [hive-keychain](https://github.com/stoodkev/hive-keychain#requestvote)
    
    [hivesigner.js](https://github.com/ecency/hivesigner-sdk#vote)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#vote)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.vote)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txvotes)
    
*   **[Related](/search/?q=vote)**

#### `vote`[](#broadcast_ops_vote)

This operation is used to cast a vote on a post/comment. The primary purpose of voting is to express Proof-of-Brain about content to the blockchain. When a vote is cast, the content is considered in the consensus rules involving author and curation rewards.

A secondary aspect to voting involves reputation, which is not part of consensus.

_Reputation Rules:_

1.  Must have non-negative reputation to effect another user’s reputation.
2.  If you are down voting another user, you must have more reputation than them to impact their reputation.

**Notes:**

*   `voter`: must be a valid account name
*   `author`: must be a valid account name
*   `permlink`: must be content created by `author`
*   `weight`: absolute value must not be more than 10000 (100.00 %).

##### Roles: `posting active owner`

##### Parameters: `voter author permlink weight`

##### Example Op:

    [
      "vote",
      {
        "voter": "hiveio",
        "author": "alice",
        "permlink": "a-post-by-alice",
        "weight": 10000
      }
    ]
    

* * *

*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/01_comment.md)
    
    [hive-keychain](https://github.com/stoodkev/hive-keychain#requestpost)
    
    [hivesigner.js](https://github.com/ecency/hivesigner-sdk#comment)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#comment)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.comment)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txcomments)
    
*   **[Related](/search/?q=comment)**

#### `comment`[](#broadcast_ops_comment)

Creates a post/comment.

**Parameters:**

*   `parent_author` - the author that comment is being submitted to, when posting a new blog this is an empty string
*   `parent_permlink` - specific post that comment is being submitted to, when posting a new blog this is an empty string
*   `author` - author of the post/comment being submitted (account name)
*   `permlink` - unique string identifier for the post, linked to the author of the post
*   `title` - human readable title of the post being submitted, this is often blank when commenting
*   `body` - body of the post/comment being submitted, or `diff-match-patch` when updating
*   `json_metadata` - JSON object string

**Rules:**

*   The “title” must not be longer than 256 bytes
*   The “title” must be UTF-8
*   The “body” must be larger than 0 bytes
*   The “body” much also be UTF-8

**Additional Parameter Definitions:**

*   `permlink` - Two authors may have the same permlink as it’s unique to the author only. For example, there could be two authors, alice and bob, and both could have a permlink of `firstpost`
*   `json_metadata` - There is no blockchain enforced validation on `json_metadata`, but the community has adopted a particular structure. It should contain a JSON object with the following keys:
    *   `tags` - An array of up to 5 strings. Although the blockchain will accept more than 5, the tags plugin only looks at the first five
    *   `app` - A user agent style application identifier. Typically `app_name/version`, e.g. `hiveblog/0.1`
    *   `format` - The format of the body, e.g. markdown
    *   In addition to the above keys, application developers are free to add any other keys they want to help manage the content they broadcast.

A typical `comment` operation would look similar to the below:

    {
      "author": "Joe",
      "title": "A post by Joe",
      "body": "Look at my awesome post",
      "parent_author": "",
      "parent_permlink": "hiveio",
      "permlink": "a-post-by-joe",
      "json_metadata": "{\"tags\":[\"hiveio\",\"example\",\"tags\"]}"
    }
    

#### Create vs. Update

When a comment is first broadcast, the `permlink` must be unique for the `author`. Otherwise, it is interpreted as an update operation. Updating will either replace the entire body with the latest operation or patch the body if using [`diff-match-patch`](https://github.com/google/diff-match-patch).

For example, if we have a paragraph that has already been broadcast:

> “It’s been quite a lot of fun working with these wonderful folk on the Open Hive Network”

And we want to change it to:

> “It’s been quite a lot of fun working with these wonderful people on the Open Hive Network”

We can broadcast the `comment` operation with the following `body`:

    - "@@ -406,12 +406,14 @@"
    - ful
    - -folk
    - +people
    - at
    

The blockchain will know that this means we have changed the word ‘folk’ to ‘people’ within that paragraph so when fetching this content, this diff will be applied.

In addition to body, the `title` and `json_metadata` fields will also be replaced by the latest operation.

See: [`comment_options`](/apidefinitions/#broadcast_ops_comment_options), [`vote`](/apidefinitions/#broadcast_ops_vote), [`custom_json`](/apidefinitions/#broadcast_ops_custom_json)

It should also be noted that a `vote` operation can accompany a `comment` and `comment_options` in the same transaction when the author self votes.

##### Roles: `posting active owner`

##### Parameters: `parent_author parent_permlink author permlink title body json_metadata`

##### Example Op:

    [
      "comment",
      {
        "parent_author": "",
        "parent_permlink": "hiveio",
        "author": "alice",
        "permlink": "a-post-by-alice",
        "title": "A Post By Alice",
        "body": "This is my post.",
        "json_metadata": "{\"tags\":[\"hiveio\",\"example\",\"tags\"]}"
      }
    ]
    

* * *

*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/02_transfer.md)
    
    [hive-keychain](https://github.com/stoodkev/hive-keychain#requesttransfer)
    
    [hivesigner.js](https://github.com/ecency/hivesigner-sdk#transfer)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#transfer)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.transfer)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txtransfers)
    
*   **[Related](/search/?q=transfer)**

#### `transfer`[](#broadcast_ops_transfer)

Transfers asset from one account to another. The memo is plain-text, any encryption on the memo is up to a higher level protocol.

**Notes:**

*   Transferring of Hive Power (VESTS) is not allowed.
*   Cannot transfer a negative amount (aka: stealing).
*   Memo must be less than 2048 bytes.
*   Memo must be UTF-8.

##### Roles: `active owner`

##### Parameters: `from to amount memo`

##### Example Op:

    [
      "transfer",
      {
        "from": "hiveio",
        "to": "alice",
        "amount": {
          "amount": "10",
          "precision": 3,
          "nai": "@@000000021"
        },
        "memo": "Thanks for all the fish."
      }
    ]
    

* * *

*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/03_transfer_to_vesting.md)
    
    [hive-keychain](https://github.com/stoodkev/hive-keychain#requestpowerup)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#transfer-to-vesting)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.transfer_to_vesting)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txtransfers)
    
*   **[Related](/search/?q=transfer%20to%20vesting)**

#### `transfer_to_vesting`[](#broadcast_ops_transfer_to_vesting)

This operation converts HIVE into VFS (Vesting Fund Shares) at the current exchange rate. With this operation it is possible to give another account vesting shares so that faucets can pre-fund new accounts with vesting shares.

**Notes:**

*   Amount must be in HIVE.
*   Must transfer a nonzero amount.

See: [delayed\_voting](/apidefinitions/#broadcast_ops_delayed_voting)

##### Roles: `active owner`

##### Parameters: `from to amount`

##### Example Op:

    [
      "transfer_to_vesting",
      {
        "from": "alice",
        "to": "",
        "amount": {
          "amount": "357000",
          "precision": 3,
          "nai": "@@000000021"
        }
      }
    ]
    

* * *

*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/04_withdraw_vesting.md)
    
    [hive-keychain](https://github.com/stoodkev/hive-keychain#requestpowerdown)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#withdraw-vesting)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.withdraw_vesting)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txwithdraws)
    
*   **[Related](/search/?q=withdraw%20vesting)**

#### `withdraw_vesting`[](#broadcast_ops_withdraw_vesting)

At any given point in time an account can be withdrawing from their vesting shares. A user may change the number of shares they wish to cash out at any time between 0 and their total vesting stake.

After applying this operation, vesting\_shares will be withdrawn at a rate of vesting\_shares/13 per week for 13 weeks starting one week after this operation is included in the blockchain.

This operation is not valid if the user has no vesting shares.

**Notes:**

*   Amount must be VESTS.

##### Roles: `active owner`

##### Parameters: `account vesting_shares`

##### Example Op:

    [
      "withdraw_vesting",
      {
        "account": "hiveio",
        "vesting_shares": {
          "amount": "200000000000",
          "precision": 6,
          "nai": "@@000000037"
        }
      }
    ]
    

* * *

*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/05_limit_order_create.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#limit-order-create)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.limit_order_create)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txlimitorders)
    
*   **[Related](/search/?q=limit%20order%20create)**

#### `limit_order_create`[](#broadcast_ops_limit_order_create)

This operation creates a limit order and matches it against existing open orders. The maximum expiration time for any limit order is 28 days from `head_block_time()`.

##### Roles: `active owner`

##### Parameters: `owner orderid amount_to_sell min_to_receive fill_or_kill expiration`

##### Example Op:

    [
      "limit_order_create",
      {
        "owner": "hiveio",
        "orderid": 10,
        "amount_to_sell": {
          "amount": "9950",
          "precision": 3,
          "nai": "@@000000021"
        },
        "min_to_receive": {
          "amount": "3500",
          "precision": 3,
          "nai": "@@000000013"
        },
        "fill_or_kill": false,
        "expiration": "2035-10-29T06:32:22"
      }
    ]
    

* * *

*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/06_limit_order_cancel.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#limit-order-cancel)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.limit_order_cancel)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txlimitorderscancels)
    
*   **[Related](/search/?q=limit%20order%20cancel)**

#### `limit_order_cancel`[](#broadcast_ops_limit_order_cancel)

Cancels an internal market order and returns the balance to owner.

##### Roles: `active owner`

##### Parameters: `owner orderid`

##### Example Op:

    [
      "limit_order_cancel",
      {"owner": "hiveio", "orderid": 10}
    ]
    

* * *

*   **[Related](/search/?q=price)**

#### `price`[](#broadcast_ops_price)

##### Roles: `active owner`

##### Parameters: `base quote`

* * *

*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/07_feed_publish.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#feed-publish)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.feed_publish)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txfeeds)
    
*   **[Related](/search/?q=feed%20publish)**

#### `feed_publish`[](#broadcast_ops_feed_publish)

Witnesses regularly publish a price feed that enables the blockchain to calculate a conversion ratio between HBD and HIVE.

Feeds can only be published by the top N witnesses which are included in every round and are used to define the exchange rate between HIVE and the US dollar.

##### Roles: `active owner`

##### Parameters: `publisher exchange_rate`

##### Example Op:

    [
      "feed_publish",
      {
        "publisher": "alice",
        "exchange_rate": {
          "base": {
            "amount": "1000",
            "precision": 3,
            "nai": "@@000000013"
          },
          "quote": {
            "amount": "1000000",
            "precision": 3,
            "nai": "@@000000021"
          }
        }
      }
    ]
    

* * *

*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/08_convert.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#convert)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.convert)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txconverts)
    
*   **[Related](/search/?q=convert)**

#### `convert`[](#broadcast_ops_convert)

This operation instructs the blockchain to start a conversion between HIVE and HBD, the funds are deposited after 3.5 days.

The identifier `requestid` will match the one found in [fill\_convert\_request](/apidefinitions/#broadcast_ops_fill_convert_request) when the request is executed.

##### Roles: `active owner`

##### Parameters: `owner requestid amount`

##### Example Op:

    [
      "convert",
      {
        "owner": "hiveio",
        "requestid": 1467592156,
        "amount": {
          "amount": "5000",
          "precision": 3,
          "nai": "@@000000013"
        }
      }
    ]
    

* * *

*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/09_account_create.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#account-create)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.account_create)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txaccountcreates)
    
*   **[Related](/search/?q=account%20create)**

#### `account_create`[](#broadcast_ops_account_create)

Broadcasted to the blockchain to create a new account.

##### Roles: `active owner`

##### Parameters: `fee creator new_account_name owner active posting memo_key json_metadata`

##### Example Op:

    [
      "account_create",
      {
        "fee": {
          "amount": "0",
          "precision": 3,
          "nai": "@@000000021"
        },
        "creator": "hiveio",
        "new_account_name": "alice",
        "owner": {
          "weight_threshold": 1,
          "account_auths": [],
          "key_auths": [
            [
              "STM5b4i9gBqvh4sbgrooXPu2dbGLewNPZkXeuNeBjyiswnu2szgXx",
              1
            ]
          ]
        },
        "active": {
          "weight_threshold": 1,
          "account_auths": [],
          "key_auths": [
            [
              "STM7ko5nzqaYfjbD4tKWGmiy3xtT9eQFZ3Pcmq5JmygTRptWSiVQy",
              1
            ]
          ]
        },
        "posting": {
          "weight_threshold": 1,
          "account_auths": [],
          "key_auths": [
            [
              "STM5xAKxnMT2y9VoVJdF63K8xRQAohsiQy9bA33aHeyMB5vgkzaay",
              1
            ]
          ]
        },
        "memo_key": "STM8ZSyzjPm48GmUuMSRufkVYkwYbZzbxeMysAVp7KFQwbTf98TcG",
        "json_metadata": "{}"
      }
    ]
    

* * *

*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/10_account_update.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#account-update)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.account_update)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txaccountupdates)
    
*   **[Related](/search/?q=account%20update)**

#### `account_update`[](#broadcast_ops_account_update)

Updates account information.

##### Roles: `active owner`

##### Parameters: `account owner active posting memo_key json_metadata`

##### Example Op:

    [
      "account_update",
      {
        "account": "hiveio",
        "posting": {
          "weight_threshold": 1,
          "account_auths": [],
          "key_auths": [
            [
              "STM6FATHLohxTN8RWWkU9ZZwVywXo6MEDjHHui1jEBYkG2tTdvMYo",
              1
            ],
            [
              "STM76EQNV2RTA6yF9TnBvGSV71mW7eW36MM7XQp24JxdoArTfKA76",
              1
            ]
          ]
        },
        "memo_key": "STM6FATHLohxTN8RWWkU9ZZwVywXo6MEDjHHui1jEBYkG2tTdvMYo",
        "json_metadata": ""
      }
    ]
    

* * *

*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/11_witness_update.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#witness-update)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.witness_update)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txwitnessupdates)
    
*   **[Related](/search/?q=witness%20update)**

#### `witness_update`[](#broadcast_ops_witness_update)

Users who wish to become a witness must apply for the position and allow voting to begin.

If the owner isn’t a witness they will become a witness. If the `block_signing_key` is null then the witness is removed from contention. The network will pick the top 21 witnesses for producing blocks.

**Notes:**

*   `url` cannot be more than 2048 bytes.
*   `url` must be UTF-8.
*   `fee` should be zero and not confused with `props["account_creation_fee"]` (see: [#410](https://github.com/steemit/steem/issues/410#issuecomment-247426741)).

##### Roles: `active owner`

##### Parameters: `owner url block_signing_key props fee`

##### Example Op:

    [
      "witness_update",
      {
        "owner": "alice",
        "url": "witness-category/my-witness",
        "block_signing_key": "STM8LoQjQqJHvotqBo7HjnqmUbFW9oJ2theyqonzUd9DdJ7YYHsvD",
        "props": {
          "account_creation_fee": {
            "amount": "100000",
            "precision": 3,
            "nai": "@@000000021"
          },
          "maximum_block_size": 131072,
          "hbd_interest_rate": 1000
        },
        "fee": {
          "amount": "0",
          "precision": 3,
          "nai": "@@000000021"
        }
      }
    ]
    

* * *

*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/12_account_witness_vote.md)
    
    [hive-keychain](https://github.com/stoodkev/hive-keychain#requestwitnessvote)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#account-witness-vote)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.account_witness_vote)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txaccountwitnessvotes)
    
*   **[Related](/search/?q=account%20witness%20vote)**

#### `account_witness_vote`[](#broadcast_ops_account_witness_vote)

All accounts with a VFS (Vesting Fund Shares) can vote for or against any witness, up to 30 witnesses. See: [`HIVE_MAX_ACCOUNT_WITNESS_VOTES`](/tutorials-recipes/understanding-configuration-values.html#HIVE_MAX_ACCOUNT_WITNESS_VOTES)

If a proxy is specified then all existing votes are removed.

##### Roles: `active owner`

##### Parameters: `account witness approve`

##### Example Op:

    [
      "account_witness_vote",
      {
        "account": "alice",
        "witness": "bob",
        "approve": true
      }
    ]
    

* * *

*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/13_account_witness_proxy.md)
    
    [hive-keychain](https://github.com/stoodkev/hive-keychain#requestproxy)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#account-witness-proxy)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.account_witness_proxy)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txaccountwitnessproxies)
    
*   **[Related](/search/?q=account%20witness%20proxy)**

#### `account_witness_proxy`[](#broadcast_ops_account_witness_proxy)

Allows one account to delegate witness votes to another account.

If a proxy is specified then all existing witness votes are removed.

Note, as of HF21, setting a witness proxy also applies to Hive DHF proposal approval. If you trust someone to cast your witness votes, it is assumed that you would also trust them to cast your proposal votes.

##### Roles: `active owner`

##### Parameters: `account proxy`

##### Example Op:

    [
      "account_witness_proxy",
      {"account": "alice", "proxy": "bob"}
    ]
    

* * *

*   **Disabled**
*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/14_pow.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#pow)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txpows)
    
*   **[Related](/search/?q=pow)**

#### `pow`[](#broadcast_ops_pow)

Disabled in HF14.

##### Roles: `active owner`

##### Parameters: `worker input signature work`

##### Example Op:

    [
      "pow",
      {
        "worker_account": "admin",
        "block_id": "000004433bd4602cf5f74dbb564183837df9cef8",
        "nonce": 82,
        "work": {
          "worker": "STM65wH1LZ7BfSHcK69SShnqCAH5xdoSZpGkUjmzHJ5GCuxEK9V5G",
          "input": "59b009f89477919f95914151cef06f28bf344dd6fb7670aca1c1f4323c80446b",
          "signature": "1f3f83209097efcd01b7d6f27ce726164323d503d6fcf4d55bfb7cb3032796f6766738b36062b5850d69447fdf9c091cbc70825df5eeacc4710a0b11ffdbf0912a",
          "work": "0b62f4837801cd857f01d6a541faeb13d6bb95f1c36c6b4b14a47df632aa6c92"
        },
        "props": {
          "account_creation_fee": {
            "amount": "100000",
            "precision": 3,
            "nai": "@@000000021"
          },
          "maximum_block_size": 131072,
          "hbd_interest_rate": 1000
        }
      }
    ]
    

* * *

*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/15_custom.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#custom)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.custom)
    
*   **[Related](/search/?q=custom)**

#### `custom`[](#broadcast_ops_custom)

Provides a generic way to add higher level protocols on top of witness consensus.

There is no validation for this operation other than that required auths are valid.

##### Roles: `active owner`

##### Parameters: `required_auths id data`

##### Example Op:

    [
      "custom",
      {
        "required_auths": ["bytemaster"],
        "id": 777,
        "data": "0a627974656d617374657207737465656d697402a3d13897d82114466ad87a74b73a53292d8331d1bd1d3082da6bfbcff19ed097029db013797711c88cccca3692407f9ff9b9ce7221aaa2d797f1692be2215d0a5f6d2a8cab6832050078bc5729201e3ea24ea9f7873e6dbdc65a6bd9899053b9acda876dc69f11a13df9ca8b26b6"
      }
    ]
    

* * *

*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/16_witness_block_approve.md)
    
*   **[Related](/search/?q=witness%20block%20approve)**

#### `witness_block_approve`[](#broadcast_ops_witness_block_approve)

This is an operation for witnesses to approve the block quicker

##### Roles: `witness_signature`

##### Parameters: `required_auths witness block_id`

* * *

*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/17_delete_comment.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#delete-comment)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.delete_comment)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txdeletecomments)
    
*   **[Related](/search/?q=delete%20comment)**

#### `delete_comment`[](#broadcast_ops_delete_comment)

A post or comment can only be deleted when it has no positive rshares applied (i.e., has no pending payout from upvotes) and has no replies. They are not really deleted from the blockchain as they are still recorded in the original block.

##### Roles: `posting active owner`

##### Parameters: `author permlink`

##### Example Op:

    [
      "delete_comment",
      {
        "author": "alice",
        "permlink": "a-post-by-alice"
      }
    ]
    

* * *

*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/18_custom_json.md)
    
    [hive-keychain](https://github.com/stoodkev/hive-keychain#requestcustomjson)
    
    [hivesigner.js](https://github.com/ecency/hivesigner-sdk#custom-json)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#custom-json)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.custom_json)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txcustoms)
    
*   **[Related](/search/?q=custom%20json)**

#### `custom_json`[](#broadcast_ops_custom_json)

Serves the same purpose as `custom` but also supports required posting authorities. Unlike `custom`, this operation is designed to be human readable/developer friendly.

##### `follow`

As of HF9, the follow plugin will track follow/unfollow/ignore events.

##### `reblog`

As of HF14, allows users to share blogs they find with those who follow them. This change implemented entirely outside the blockchain consensus which means that reblogging does not create a new post, it merely shares an existing post with people who follow you.

##### `witness`

As of HF18, the witness plugin has a custom operation called `enable_content_editing` that allows a user to signal they want to edit their content. By consensus, content is editable indefinitely, but is soft forked to be frozen after payout. This operation requires an `active` key and is designed to prevent vandalism if a posting key is compromised. [#1017](https://archive.is/G7XUv)

##### Roles: `posting active owner`

##### Parameters: `required_auths required_posting_auths id json`

##### Example Op:

    [
      "custom_json",
      {
        "required_auths": [],
        "required_posting_auths": ["hiveio"],
        "id": "follow",
        "json": "[\"follow\",{\"follower\":\"hiveio\",\"following\":\"alice\",\"what\":[\"blog\"]}]"
      }
    ]
    

    [
      "custom_json",
      {
        "required_auths": [],
        "required_posting_auths": ["alice"],
        "id": "follow",
        "json": "[\"follow\",{\"follower\":\"alice\",\"following\":\"eve\",\"what\":[\"ignore\"]}]"
      }
    ]
    

    [
      "custom_json",
      {
        "required_auths": [],
        "required_posting_auths": ["bob"],
        "id": "reblog",
        "json": "[\"reblog\", {\"account\":\"bob\",\"author\":\"alice\",\"permlink\":\"a-post-by-alice\"}]"
      }
    ]
    

    [
      "custom_json",
      {
        "required_auths": ["alice"],
        "required_posting_auths": [],
        "id": "witness",
        "json": "[\"enable_content_editing\", {\"account\": \"alice\", \"relock_time\": \"2100-01-01T12:00:00\"}]"
      }
    ]
    

* * *

*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/19_comment_options.md)
    
    [hive-keychain](https://github.com/stoodkev/hive-keychain#requestpost)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#comment-options)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.comment)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txcommentsoptions)
    
*   **[Related](/search/?q=comment%20options)**

#### `comment_options`[](#broadcast_ops_comment_options)

Authors of posts may not want all of the benefits that come from creating a post. This operation allows authors to update properties associated with their post.

Typically, these options will accompany a `comment` operation in the same transaction.

As of HF17, content can specify beneficiaries to receive a part of their author rewards. The beneficiaries are specified in the extension field of the `comment_options_operation` and is a sorted vector (by account name) of account name, weight pairs. The beneficiaries can only be specified once and must be specified before any votes are cast on the comment. Most apps are already adding a `comment_options` in the transaction that creates the comment, so this should not be much of a challenge to add to existing apps.

**Notes:**

*   The max\_accepted\_payout may be decreased, but never increased.
*   The percent\_hbd may be decreased, but never increased.
*   Part of `comment_option` validation process, to be called when `allowed_vote_assets` object has been added as comment option extension are:
    *   When votable assets are greater than maximum votable assets: _“Too much votable assets specified”_
    *   When the symbol is not allowed in the list for votable assets: _“HIVE can not be explicitly specified as one of allowed\_vote\_assets”_
*   `max_accepted_payout`: HBD value of the maximum payout this post will receive
*   `percent_hbd`: the percent of Hive Dollars to key, unkept amounts will be received as Hive Power
*   `allow_votes`: allows/disallows a post to receive votes;
*   `allow_curation_rewards`: allows/disllows voters to recieve curation rewards. Rewards return to reward fund.
*   `beneficiaries`
    *   Must have at least one (empty `beneficiaries` not allowed).
    *   Cannot have more than 127 (witness currently only allow up to 8).
    *   Cannot allocate more than 100% of rewards to one account.
    *   Cannot allocate more than 100% of rewards to a comment.
    *   Must be specified in sorted order (account ascending; no duplicates).

##### Roles: `posting active owner`

##### Parameters: `author permlink max_accepted_payout percent_hbd allow_votes allow_curation_rewards extensions`

##### Example Op:

    [
      "comment_options",
      {
        "author": "alice",
        "permlink": "a-post-by-alice",
        "max_accepted_payout": {
          "amount": "1000000",
          "precision": 3,
          "nai": "@@000000013"
        },
        "percent_hbd": 5000,
        "allow_votes": true,
        "allow_curation_rewards": true,
        "extensions": []
      }
    ]
    

    [
      "comment_options",
      {
        "author": "bob",
        "permlink": "a-post-with-a-beneficiary",
        "max_accepted_payout": {
          "amount": "1000000",
          "precision": 3,
          "nai": "@@000000013"
        },
        "percent_hbd": 63,
        "allow_votes": true,
        "allow_curation_rewards": true,
        "extensions": [
          [
            0,
            {
              "beneficiaries": [{"account": "charlie", "weight": 1000}]
            }
          ]
        ]
      }
    ]
    

    [
      "comment_options",
      {
        "author": "charlie",
        "permlink": "a-post-with-multiple-beneficiaries",
        "max_accepted_payout": {
          "amount": "1000000",
          "precision": 3,
          "nai": "@@000000013"
        },
        "percent_hbd": 62688,
        "allow_votes": true,
        "allow_curation_rewards": true,
        "extensions": [
          [
            0,
            {
              "beneficiaries": [
                {"account": "david", "weight": 500},
                {"account": "erin", "weight": 500},
                {"account": "faythe", "weight": 1000},
                {"account": "frank", "weight": 500}
              ]
            }
          ]
        ]
      }
    ]
    

* * *

*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/20_set_withdraw_vesting_route.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#set-withdraw-vesting-route)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.set_withdraw_vesting_route)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txwithdrawvestingroutes)
    
*   **[Related](/search/?q=set%20withdraw%20vesting%20route)**

#### `set_withdraw_vesting_route`[](#broadcast_ops_set_withdraw_vesting_route)

Allows an account to setup a vesting withdraw but with the additional request for the funds to be transferred directly to another account’s balance rather than the withdrawing account. In addition, those funds can be immediately vested again, circumventing the conversion from vests to hive and back, guaranteeing they maintain their value.

**Notes:**

*   Percent must be valid hive percent.

##### Roles: `active owner`

##### Parameters: `from_account to_account percent auto_vest`

##### Example Op:

    [
      "set_withdraw_vesting_route",
      {
        "from_account": "alice",
        "to_account": "bob",
        "percent": 10000,
        "auto_vest": true
      }
    ]
    

* * *

*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/21_limit_order_create2.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#limit-order-create2)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txlimitorders)
    
*   **[Related](/search/?q=limit%20order%20create2)**

#### `limit_order_create2`[](#broadcast_ops_limit_order_create2)

This operation is identical to `limit_order_create` except it serializes the price rather than calculating it from other fields. The maximum expiration time for any limit order is 28 days from `head_block_time()`.

*   For prices involving Hive Dollars (HBD), the base asset must be HBD.
*   For prices involving SMT assets, the base asset must be HIVE.
*   The quote must be a power of 10.

See: [#1573](https://archive.ph/iYvnP)

##### Roles: `active owner`

##### Parameters: `owner orderid amount_to_sell exchange_rate fill_or_kill expiration`

##### Example Op:

    [
      "limit_order_create2",
      {
        "owner": "alice",
        "orderid": 492991,
        "amount_to_sell": {
          "amount": "1",
          "precision": 3,
          "nai": "@@000000013"
        },
        "exchange_rate": {
          "base": {
            "amount": "1",
            "precision": 3,
            "nai": "@@000000013"
          },
          "quote": {
            "amount": "10",
            "precision": 3,
            "nai": "@@000000021"
          }
        },
        "fill_or_kill": false,
        "expiration": "2017-05-12T23:11:13"
      }
    ]
    

* * *

*   **Since: HF20**
*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/22_claim_account.md)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.claim_account)
    
*   **[Related](/search/?q=claim%20account)**

#### `claim_account`[](#broadcast_ops_claim_account)

Requests from users or dApps to get an account creation ticket in order to create new accounts. These operations are issued before the actual creation of the account on the blockchain.

See: [0.20.2 Release Notes](https://archive.is/1T93t)

##### Roles: `active owner`

##### Parameters: `fee creator extensions`

##### Example Op:

    [
      "claim_account",
      {
        "fee": {
          "amount": "0",
          "precision": 3,
          "nai": "@@000000021"
        },
        "creator": "hiveio",
        "extensions": []
      }
    ]
    

* * *

*   **Since: HF20**
*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/23_create_claimed_account.md)
    
    [hive-keychain](https://github.com/stoodkev/hive-keychain#requestcreateclaimedaccount)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.create_claimed_account)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txaccountcreates)
    
*   **[Related](/search/?q=create%20claimed%20account)**

#### `create_claimed_account`[](#broadcast_ops_create_claimed_account)

When used with `claim_account`, works identically to `account_create`. See: [0.20.2 Release Notes](https://archive.is/1T93t)

##### Roles: `active owner`

##### Parameters: `creator new_account_name owner active posting memo_key json_metadata`

##### Example Op:

    [
      "create_claimed_account",
      {
        "creator": "hiveio",
        "new_account_name": "alice",
        "owner": {
          "weight_threshold": 1,
          "account_auths": [],
          "key_auths": [
            [
              "STM5b4i9gBqvh4sbgrooXPu2dbGLewNPZkXeuNeBjyiswnu2szgXx",
              1
            ]
          ]
        },
        "active": {
          "weight_threshold": 1,
          "account_auths": [],
          "key_auths": [
            [
              "STM7ko5nzqaYfjbD4tKWGmiy3xtT9eQFZ3Pcmq5JmygTRptWSiVQy",
              1
            ]
          ]
        },
        "posting": {
          "weight_threshold": 1,
          "account_auths": [],
          "key_auths": [
            [
              "STM5xAKxnMT2y9VoVJdF63K8xRQAohsiQy9bA33aHeyMB5vgkzaay",
              1
            ]
          ]
        },
        "memo_key": "STM8ZSyzjPm48GmUuMSRufkVYkwYbZzbxeMysAVp7KFQwbTf98TcG",
        "json_metadata": "{}"
      }
    ]
    

* * *

*   **Since: HF11**
*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/24_request_account_recovery.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#request-account-recovery)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.request_account_recovery)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txaccountrecovers)
    
*   **[Related](/search/?q=request%20account%20recovery)**

#### `request_account_recovery`[](#broadcast_ops_request_account_recovery)

All account recovery requests come from a listed recovery account. This is secure based on the assumption that only a trusted account should be a recovery account. It is the responsibility of the recovery account to verify the identity of the account holder of the account to recover by whichever means they have agreed upon. The blockchain assumes identity has been verified when this operation is broadcast.

This operation creates an account recovery request which the account to recover has 24 hours to respond to before the request expires and is invalidated.

There can only be one active recovery request per account at any one time. Pushing this operation for an account to recover when it already has an active request will either update the request to a new new owner authority and extend the request expiration to 24 hours from the current head block time or it will delete the request. To cancel a request, simply set the weight threshold of the new owner authority to 0, making it an open authority.

Additionally, the new owner authority must be satisfiable. In other words, the sum of the key weights must be greater than or equal to the weight threshold.

This operation only needs to be signed by the the recovery account. The account to recover confirms its identity to the blockchain in the recover account operation.

**Notes:**

*   `recovery_account`: The recovery account is listed as the recovery account on the account to recover.
*   `account_to_recover`: The account to recover. This is likely due to a compromised owner authority.
*   `new_owner_authority`: The new owner authority the account to recover wishes to have. This is secret known by the account to recover and will be confirmed in a `recover_account`.

See: [#169](https://archive.is/4eLqu)

##### Roles: `active owner`

##### Parameters: `recovery_account account_to_recover new_owner_authority extensions`

##### Example Op:

    [
      "request_account_recovery",
      {
        "recovery_account": "hiveio",
        "account_to_recover": "alice",
        "new_owner_authority": {
          "weight_threshold": 1,
          "account_auths": [],
          "key_auths": [
            [
              "STM6LYxj96zdypHYqgDdD6Nyh2NxerN3P1Mp3ddNm7gci63nfrSuZ",
              1
            ]
          ]
        },
        "extensions": []
      }
    ]
    

* * *

*   **Since: HF11**
*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/25_recover_account.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#recover-account)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.recover_account)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txaccountrecoveryconfirms)
    
*   **[Related](/search/?q=recover%20account)**

#### `recover_account`[](#broadcast_ops_recover_account)

Broadcasted to the blockchain by the hacked account’s owner to confirm the account recovery request sent by its Recovery Account.

##### Roles: `owner`

##### Parameters: `account_to_recover new_owner_authority recent_owner_authority extensions`

##### Example Op:

    [
      "recover_account",
      {
        "account_to_recover": "alice",
        "new_owner_authority": {
          "weight_threshold": 1,
          "account_auths": [],
          "key_auths": [
            [
              "STM7j3nhkhHTpXqLEvdx2yEGhQeeorTcxSV6WDL2DZGxwUxYGrHvh",
              1
            ]
          ]
        },
        "recent_owner_authority": {
          "weight_threshold": 1,
          "account_auths": [],
          "key_auths": [
            [
              "STM78Xth94gNxp8nmByFV2vNAhg9bsSdviJ6fQXUTFikySLK3uTxC",
              1
            ]
          ]
        },
        "extensions": []
      }
    ]
    

* * *

*   **Since: HF11**
*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/26_change_recovery_account.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#change-recovery-account)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.change_recovery_account)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txaccountrecoverychanges)
    
*   **[Related](/search/?q=change%20recovery%20account)**

#### `change_recovery_account`[](#broadcast_ops_change_recovery_account)

Each account lists another account as their recovery account. The recovery account has the ability to create `account_recovery_requests` for the account to recover. An account can change their recovery account at any time with a 30 day delay. This delay is to prevent an attacker from changing the recovery account to a malicious account during an attack. These 30 days match the 30 days that an owner authority is valid for recovery purposes.

On account creation the recovery account is set either to the creator of the account (The account that pays the creation fee and is a signer on the transaction) or to the empty string if the account was mined. An account with no recovery has the top voted witness as a recovery account, at the time the recover request is created. Note: This does mean the effective recovery account of an account with no listed recovery account can change at any time as witness vote weights. The top voted witness is explicitly the most trusted witness according to stake.

See: [#169](https://archive.is/4eLqu), [PY: Account Recovery](/tutorials-python/account_recovery.html)

##### Roles: `owner`

##### Parameters: `account_to_recover new_recovery_account extensions`

##### Example Op:

    [
      "change_recovery_account",
      {
        "account_to_recover": "alice",
        "new_recovery_account": "bob",
        "extensions": []
      }
    ]
    

* * *

*   **Since: HF14**
*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/27_escrow_transfer.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#escrow-transfer)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.escrow_transfer)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txescrowtransfers)
    
*   **[Related](/search/?q=escrow%20transfer)**

#### `escrow_transfer`[](#broadcast_ops_escrow_transfer)

The purpose of this operation is to enable someone to send money contingently to another individual. The funds leave the _from_ account and go into a temporary balance where they are held until _from_ releases it to _to_ or _to_ refunds it to _from_.

In the event of a dispute the _agent_ can divide the funds between the to/from account. Disputes can be raised any time before or on the dispute deadline time, after the escrow has been approved by all parties.

This operation only creates a proposed escrow transfer. Both the _agent_ and _to_ must agree to the terms of the arrangement by approving the escrow.

The escrow agent is paid the fee on approval of all parties. It is up to the escrow agent to determine the fee.

Escrow transactions are uniquely identified by `from` and `escrow_id`, the `escrow_id` is defined by the sender.

See: [hive\_operations.hpp:299](https://gitlab.syncad.com/hive/hive/-/blob/2074917f0735d9bdf22d33f5bdb089df3f6361b0/libraries/protocol/include/hive/protocol/hive_operations.hpp#L299-335)

##### Roles: `active owner`

##### Parameters: `from to agent escrow_id hbd_amount hive_amount fee ratification_deadline escrow_expiration json_meta`

##### Example Op:

    [
      "escrow_transfer",
      {
        "from": "alice",
        "to": "bob",
        "hbd_amount": {
          "amount": "1000",
          "precision": 3,
          "nai": "@@000000013"
        },
        "hive_amount": {
          "amount": "0",
          "precision": 3,
          "nai": "@@000000021"
        },
        "escrow_id": 23456789,
        "agent": "charlie",
        "fee": {
          "amount": "100",
          "precision": 3,
          "nai": "@@000000013"
        },
        "json_meta": "{}",
        "ratification_deadline": "2017-02-26T11:22:39",
        "escrow_expiration": "2017-02-28T11:22:39"
      }
    ]
    

* * *

*   **Since: HF14**
*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/28_escrow_dispute.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#escrow-dispute)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.escrow_dispute)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txescrowdisputes)
    
*   **[Related](/search/?q=escrow%20dispute)**

#### `escrow_dispute`[](#broadcast_ops_escrow_dispute)

If either the sender or receiver of an escrow payment has an issue, they can raise it for dispute. Once a payment is in dispute, the agent has authority over who gets what.

See: [hive\_operations.hpp:299](https://gitlab.syncad.com/hive/hive/-/blob/2074917f0735d9bdf22d33f5bdb089df3f6361b0/libraries/protocol/include/hive/protocol/hive_operations.hpp#L299-335)

##### Roles: `active owner`

##### Parameters: `from to agent who escrow_id`

##### Example Op:

    [
      "escrow_dispute",
      {
        "from": "alice",
        "to": "bob",
        "agent": "charlie",
        "who": "alice",
        "escrow_id": 72526562
      }
    ]
    

* * *

*   **Since: HF14**
*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/29_escrow_release.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#escrow-release)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.escrow_release)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txescrowreleases)
    
*   **[Related](/search/?q=escrow%20release)**

#### `escrow_release`[](#broadcast_ops_escrow_release)

This operation can be used by anyone associated with the escrow transfer to release funds if they have permission.

The permission scheme is as follows:

*   If there is no dispute and escrow has not expired, either party can release funds to the other.
*   If escrow expires and there is no dispute, either party can release funds to either party.
*   If there is a dispute regardless of expiration, the agent can release funds to either party following whichever agreement was in place between the parties.

After the expiration, the receiver can use this operation to claim the funds. If the funds are not claimed by the receiver within 1 month of expiration then the sender can reclaim the funds.

See: [hive\_operations.hpp:299](https://gitlab.syncad.com/hive/hive/-/blob/2074917f0735d9bdf22d33f5bdb089df3f6361b0/libraries/protocol/include/hive/protocol/hive_operations.hpp#L299-335)

##### Roles: `active owner`

##### Parameters: `from to agent who receiver escrow_id hbd_amount hive_amount`

##### Example Op:

    [
      "escrow_release",
      {
        "from": "alice",
        "to": "bob",
        "agent": "charlie",
        "who": "charlie",
        "receiver": "bob",
        "escrow_id": 72526562,
        "hbd_amount": {
          "amount": "5000",
          "precision": 3,
          "nai": "@@000000013"
        },
        "hive_amount": {
          "amount": "0",
          "precision": 3,
          "nai": "@@000000021"
        }
      }
    ]
    

* * *

*   **Disabled**
*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/30_pow2.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#pow2)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txpows)
    
*   **[Related](/search/?q=pow2)**

#### `pow2`[](#broadcast_ops_pow2)

Disabled in HF17.

##### Roles: `active owner`

##### Parameters: `input pow_summary`

##### Example Op:

    [
      "pow2",
      {
        "work": [
          0,
          {
            "input": {
              "worker_account": "alice",
              "prev_block": "003ea604345523c344fbadab605073ea712dd76f",
              "nonce": "1052853013628665497"
            },
            "pow_summary": 3817904373
          }
        ],
        "props": {
          "account_creation_fee": {
            "amount": "1",
            "precision": 3,
            "nai": "@@000000021"
          },
          "maximum_block_size": 131072,
          "hbd_interest_rate": 1000
        }
      }
    ]
    

* * *

*   **Since: HF14**
*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/31_escrow_approve.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#escrow-approve)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.escrow_approve)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txescrowapproves)
    
*   **[Related](/search/?q=escrow%20approve)**

#### `escrow_approve`[](#broadcast_ops_escrow_approve)

After creating an escrow transaction, both the receiver or the agent can approve or disapprove the deal. If nobody approves or disapproves the transaction before the deadline date, the funds are returned to the sender.

The agent and to accounts must approve an escrow transaction for it to be valid on the blockchain. Once a party approves the escrow, they cannot revoke their approval. Subsequent escrow approve operations, regardless of the approval, will be rejected.

See: [hive\_operations.hpp:299](https://gitlab.syncad.com/hive/hive/-/blob/2074917f0735d9bdf22d33f5bdb089df3f6361b0/libraries/protocol/include/hive/protocol/hive_operations.hpp#L299-335)

##### Roles: `active owner`

##### Parameters: `from to agent who escrow_id approve`

##### Example Op:

    [
      "escrow_approve",
      {
        "from": "alice",
        "to": "bob",
        "agent": "charlie",
        "who": "charlie",
        "escrow_id": 59102208,
        "approve": true
      }
    ]
    

* * *

*   **Since: HF14**
*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/32_transfer_to_savings.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#transfer-to-savings)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.transfer_to_savings)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txtransfers)
    
*   **[Related](/search/?q=transfer%20to%20savings)**

#### `transfer_to_savings`[](#broadcast_ops_transfer_to_savings)

For time locked savings accounts. A user can place Hive and Hive Dollars into time locked savings balances. Funds can be withdrawn from these balances after a three day delay. The point of this addition is to mitigate loss from hacked and compromised account. The max a user can lose instantaneously is the sum of what the hold in liquid balances. Assuming an account can be recovered quickly, loss in such situations can be kept to a minimum.

See: [hive\_operations.hpp:988](https://gitlab.syncad.com/hive/hive/-/blob/2074917f0735d9bdf22d33f5bdb089df3f6361b0/libraries/protocol/include/hive/protocol/hive_operations.hpp#L988-996)

##### Roles: `active owner`

##### Parameters: `from to amount memo`

##### Example Op:

    [
      "transfer_to_savings",
      {
        "from": "alice",
        "to": "alice",
        "amount": {
          "amount": "1000",
          "precision": 3,
          "nai": "@@000000013"
        },
        "memo": ""
      }
    ]
    

* * *

*   **Since: HF14**
*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/33_transfer_from_savings.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#transfer-from-savings)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.transfer_from_savings)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txtransfers)
    
*   **[Related](/search/?q=transfer%20from%20savings)**

#### `transfer_from_savings`[](#broadcast_ops_transfer_from_savings)

Funds withdrawals from the savings to an account take three days. Their execution is recorded in the blockchain with the [`fill_transfer_from_savings`](/apidefinitions/#broadcast_ops_fill_transfer_from_savings) virtual operation.

##### Roles: `active owner`

##### Parameters: `from request_id to amount memo`

##### Example Op:

    [
      "transfer_from_savings",
      {
        "from": "alice",
        "request_id": 101,
        "to": "alice",
        "amount": {
          "amount": "1000",
          "precision": 3,
          "nai": "@@000000013"
        },
        "memo": ""
      }
    ]
    

* * *

*   **Since: HF14**
*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/34_cancel_transfer_from_savings.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#cancel-transfer-from-savings)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.cancel_transfer_from_savings)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txtransfers)
    
*   **[Related](/search/?q=cancel%20transfer%20from%20savings)**

#### `cancel_transfer_from_savings`[](#broadcast_ops_cancel_transfer_from_savings)

Funds withdrawals from the savings can be canceled at any time before it is executed.

##### Roles: `active owner`

##### Parameters: `from request_id`

##### Example Op:

    [
      "cancel_transfer_from_savings",
      {"from": "alice", "request_id": 1}
    ]
    

* * *

*   **Since: HF14**
*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/36_decline_voting_rights.md)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.decline_voting_rights)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txdeclinevotingrights)
    
*   **[Related](/search/?q=decline%20voting%20rights)**

#### `decline_voting_rights`[](#broadcast_ops_decline_voting_rights)

An account can chose to decline their voting rights after a 30 day delay. This includes voting on content and witnesses. The voting rights cannot be acquired again once they have been declined. This is only to formalize a smart contract between certain accounts and the community that currently only exists as a social contract.

See: [hive\_operations.hpp:1020](https://gitlab.syncad.com/hive/hive/-/blob/2074917f0735d9bdf22d33f5bdb089df3f6361b0/libraries/protocol/include/hive/protocol/hive_operations.hpp#L1020-1027)

##### Roles: `owner`

##### Parameters: `account decline`

##### Example Op:

    [
      "decline_voting_rights",
      {"account": "judy", "decline": true}
    ]
    

* * *

*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/39_claim_reward_balance.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#claim-reward-balance)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.claim_reward_balance)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txclaimrewardbalances)
    
*   **[Related](/search/?q=claim%20reward%20balance)**

#### `claim_reward_balance`[](#broadcast_ops_claim_reward_balance)

Author and curator rewards are not automatically transferred to the account’s balances. One has to issue a `claim_reward_balance` operation to trigger the transfer from the reward pool to its balance.

##### Roles: `posting active owner`

##### Parameters: `account reward_hive reward_hbd reward_vests`

##### Example Op:

    [
      "claim_reward_balance",
      {
        "account": "alice",
        "reward_hive": {
          "amount": "17",
          "precision": 3,
          "nai": "@@000000021"
        },
        "reward_hbd": {
          "amount": "11",
          "precision": 3,
          "nai": "@@000000013"
        },
        "reward_vests": {
          "amount": "185025103",
          "precision": 6,
          "nai": "@@000000037"
        }
      }
    ]
    

* * *

*   **Since: HF17**
*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/40_delegate_vesting_shares.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#delegate-vesting-shares)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.delegate_vesting_shares)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txdelegatevestingshares)
    
*   **[Related](/search/?q=delegate%20vesting%20shares)**

#### `delegate_vesting_shares`[](#broadcast_ops_delegate_vesting_shares)

Delegate vesting shares from one account to the other. The vesting shares are still owned by the original account, but content voting rights and resource credit are transferred to the receiving account. This sets the delegation to `vesting_shares`, increasing it or decreasing it as needed (i.e. a delegation of 0 removes the delegation).

When a delegation is removed the shares are placed in limbo for a week to prevent using them and voting on the same content twice.

Also see:

*   [hive\_evaluator.cpp:2309](https://gitlab.syncad.com/hive/hive/-/blob/4b19e00dd6a76699aa4de1c0d50aad392cd2d0b6/libraries/hive_evaluator.cpp#L2309)

##### Roles: `active owner`

##### Parameters: `delegator delegatee vesting_shares`

##### Example Op:

    [
      "delegate_vesting_shares",
      {
        "delegator": "alice",
        "delegatee": "bob",
        "vesting_shares": {
          "amount": "94599167138276",
          "precision": 6,
          "nai": "@@000000037"
        }
      }
    ]
    

* * *

*   **Since: HF17**
*   **Deprecated**
*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/41_account_create_with_delegation.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#account-create-with-delegation)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.account_create_with_delegation)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txaccountcreates)
    
*   **[Related](/search/?q=account%20create%20with%20delegation)**

#### `account_create_with_delegation`[](#broadcast_ops_account_create_with_delegation)

**Deprecated as of HF20** If an account creation service would still like to provide a delegation of Hive Power to the accounts they create, they can still follow the account creation operation with an additional call to `delegate_vesting_shares` to add a delegation of HP to the account.

> Instead of paying the entire account creation fee with Hive, creators can now pay a smaller fee (30x less) and delegate some Hive Power for 30 days. The exact amount is 5 \* min\_fee + HIVE\_POWER == 150 \* min\_fee. You can pay any combination of HIVE and Hive Power along that curve (so long as the minimum fee is paid).

> _The witness voted HIVE fee is now the minimum required HIVE fee for delegation. Witnesses should reduce their fee by 30x when the hardfork goes live to preserve the same required fee for an all HIVE account creation._

Also see:

*   [config.hpp:145](https://gitlab.syncad.com/hive/hive/-/blob/65c58af34971416057e142ac1332421e2228749b/libraries/protocol/include/steem/protocol/config.hpp#L145)
*   [hive\_evaluator.cpp:400](https://gitlab.syncad.com/hive/hive/-/blob/4b19e00dd6a76699aa4de1c0d50aad392cd2d0b6/libraries/hive_evaluator.cpp#L400)

##### Roles: `active owner`

##### Parameters: `fee delegation creator new_account_name owner active posting memo_key json_metadata extensions`

##### Example Op:

    [
      "account_create_with_delegation",
      {
        "fee": {
          "amount": "3000",
          "precision": 3,
          "nai": "@@000000021"
        },
        "delegation": {
          "amount": "0",
          "precision": 6,
          "nai": "@@000000037"
        },
        "creator": "hiveio",
        "new_account_name": "alice",
        "owner": {
          "weight_threshold": 1,
          "account_auths": [],
          "key_auths": [
            [
              "STM5Tki3ecCdCCHCjhhwvQvXuKryL2s34Ma6CXsRzntSUTYVYxCQ9",
              1
            ]
          ]
        },
        "active": {
          "weight_threshold": 1,
          "account_auths": [],
          "key_auths": [
            [
              "STM6LUoAA8gCL9tHRz7v9xcwR4ZWD3KDRHP5t1U7UAZHdfanLxyBE",
              1
            ]
          ]
        },
        "posting": {
          "weight_threshold": 1,
          "account_auths": [],
          "key_auths": [
            [
              "STM8anmpHdfVE4AmwsDpcSXpRsydHysEbv6vGJkRQy1d1CC83zeTA",
              1
            ]
          ]
        },
        "memo_key": "STM67RYDyEkP1Ja1jFehJ45BFGA9oHHUnRnYbxKJEtMhVQiHW3S3k",
        "json_metadata": "{}",
        "extensions": []
      }
    ]
    

* * *

*   **Since: HF20**
*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/42_witness_set_properties.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#witness-set-properties)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.witness_set_properties)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txwitnesssetproperties)
    
*   **[Related](/search/?q=witness%20set%20properties)**

#### `witness_set_properties`[](#broadcast_ops_witness_set_properties)

Added in HF20 to replace the `witness_update` which was not easily extendable. While it is recommended to use `witness_set_properties`, `witness_update` will continue to work. See: [Witness Parameters](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/witness_parameters.md)

##### Roles: `block_signing active owner`

##### Parameters: `owner props extensions`

##### Example Op:

    [
      "witness_set_properties",
      {
        "owner": "alice",
        "props": {
          "account_creation_fee": "0.000 HIVE",
          "account_subsidy_budget": 10000,
          "account_subsidy_decay": 330782,
          "maximum_block_size": 65536,
          "hbd_interest_rate": "0.000 HIVE",
          "hbd_exchange_rate": {"base": "0.000 HBD", "quote": "0.000 HIVE"},
          "url": "68747470733A2F2F737465656D69742E636F6D",
          "new_signing_key": "25688bbe7b1204f26e40be054c8b2ff1997eec6d4e7be6a105aab8a0e6f11c616d7cb6066"
        },
        "extensions": []
      }
    ]
    

* * *

*   **Since: HF21**
*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/43_account_update2.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#account-update2)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.account_update2)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txaccountupdates2)
    
*   **[Related](/search/?q=account%20update2)**

#### `account_update2`[](#broadcast_ops_account_update2)

This operation behaves identically to the existing `account_update_operation` except that it allows the posting authority to sign when the owner and active authorities and memo key are not present (i.e. only valid for posting and JSON metadata).

See: [#3274](https://archive.ph/RwOyl)

##### Roles: `posting active owner`

##### Parameters: `account owner active posting memo_key json_metadata posting_json_metadata`

##### Example Op:

    [
      "account_update",
      {
        "account": "hiveio",
        "posting_json_metadata": ""
      }
    ]
    

* * *

*   **Since: HF21**
*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/44_create_proposal.md)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.create_proposal)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txproposalcreates)
    
*   **[Related](/search/?q=create%20proposal)**

#### `create_proposal`[](#broadcast_ops_create_proposal)

Creates a new proposal.

##### Roles: `postingactive owner`

##### Parameters: `creator receiver start_date end_date daily_pay subject permlink`

##### Example Op:

    [
      "create_proposal",
      {
        "creator": "alice",
        "receiver": "bob",
        "start_date": "2019-08-26T11:22:39",
        "end_date": "2019-08-26T11:22:39",
        "daily_pay": {
          "amount": "3000",
          "precision": 3,
          "nai": "@@000000013"
        },
        "subject": "subject",
        "permlink": "creator-proposal-permlink"
      }
    ]
    

* * *

*   **Since: HF21**
*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/45_update_proposal_votes.md)
    
    [hive-keychain](https://github.com/stoodkev/hive-keychain#requestupdateproposalvote)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.blockchaininstance.html?#beem.blockchaininstance.BlockChainInstance.update_proposal_votes)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.update_proposal_votes)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txproposalvoteupdates)
    
*   **[Related](/search/?q=update%20proposal%20votes)**

#### `update_proposal_votes`[](#broadcast_ops_update_proposal_votes)

Update proposal votes by `proposal.id`.

Note, proposal votes are only summed at payment time (once per hour) and may not be reported immediately by related API.

##### Roles: `posting active owner`

##### Parameters: `voter proposal_ids approve`

##### Example Op:

    [
      "update_proposal_votes",
      {
        "voter": "alice",
        "proposal_ids": [0],
        "approve": true,
        "extensions": []
      }
    ]
    

* * *

*   **Since: HF21**
*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/46_remove_proposal.md)
    
    [hive-keychain](https://github.com/stoodkev/hive-keychain#requestremoveproposal)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.remove_proposal)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txproposalremoves)
    
*   **[Related](/search/?q=remove%20proposal)**

#### `remove_proposal`[](#broadcast_ops_remove_proposal)

Removes proposal using `proposal.id` of a given proposal.

##### Roles: `posting active owner`

##### Parameters: `creator proposal_ids`

##### Example Op:

    [
      "remove_proposal",
      {"creator": "alice", "proposal_ids": [0]}
    ]
    

* * *

*   **Since: HF24**
*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/47_update_proposal.md)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.update_proposal)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txproposalupdates)
    
*   **[Related](/search/?q=update%20proposal)**

#### `update_proposal`[](#broadcast_ops_update_proposal)

Update a proposal using `proposal.id` of a given proposal. Allows creator to lower `daily_pay` but not increase it, change subject, and point to a new permlink.

##### Roles: `posting active owner`

##### Parameters: `proposal_id creator daily_pay subject permlink`

##### Example Op:

    [
      "update_proposal",
      {
        "proposal_id": 0,
        "creator": "alice",
        "daily_pay": {
          "amount": "3000",
          "precision": 3,
          "nai": "@@000000013"
        },
        "subject": "New Subject",
        "permlink": "creator-proposal-permlink"
      }
    ]
    

* * *

*   **Since: HF25**
*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/48_collateralized_convert.md)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/-/blob/master/doc/README.md#collateralized-convert)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txcollateralizedconverts-hf25)
    
*   **[Related](/search/?q=collateralized%20convert)**

#### `collateralized_convert`[](#broadcast_ops_collateralized_convert)

The `collateralized_convert` operation is similar to `convert` operation (see: [convert](/apidefinitions/#broadcast_ops_convert)), and instructs the blockchain to convert HIVE to HBD. The operation is performed after a 3.5 days delay, but the owner gets HBD immediately. The price risk is cushioned by extra HIVE. After actual conversion takes place the excess HIVE is returned to the owner.

##### Roles:

##### Parameters: `owner requestid amount`

##### Example Op:

    [
      "collateralized_convert",
      {
        "owner": "hiveio",
        "requestid": 1467592156,
        "amount": {
          "amount": "5000",
          "precision": 3,
          "nai": "@@000000021"
        }
      }
    ]
    

* * *

*   **Since: HF25**
*   **SDK Reference**
    
    [openApi](https://gitlab.syncad.com/hive/hive/-/blob/master/doc/devs/operations/49_recurrent_transfer.md)
    
    [hivesql](https://docs.hivesql.io/technical-informations/operations/txrecurrenttransfers-hf25)
    
*   **[Related](/search/?q=recurrent%20transfer)**

#### `recurrent_transfer`[](#broadcast_ops_recurrent_transfer)

The `recurrent_transfer` operation creates/updates/removes a recurrent transfer (transfers any liquid asset every fixed amount of time from one account to another). If amount is set to 0, the recurrent transfer is be deleted. If there is already a recurrent transfer matching from and to, the recurrent transfer is updated.

Also see: [database\_api.find\_recurrent\_transfers](/apidefinitions/#database_api.find_recurrent_transfers)

##### Roles:

##### Parameters: `from to amount memo recurrence executions extensions`

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#prove-authority)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
*   **[Related](/search/?q=prove%20authority)**

#### `prove_authority`[](#broadcast_ops_prove_authority)

##### Roles: `active owner`

##### Parameters: `challenged require_owner`

* * *

*   **Since: HF14**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#custom-binary)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.custom_binary)
    
*   **[Related](/search/?q=custom%20binary)**

#### `custom_binary`[](#broadcast_ops_custom_binary)

The semmantics for this operation are the same as the `custom_json` operation, but with a binary payload. The json deserialization has a non-trivial cost associated with it. This operation will allow for binary deserialization of plugin operations and should improve overall performance of plugins that chose to use it.

See: [hive\_operations.hpp:604](https://gitlab.syncad.com/hive/hive/-/blob/2074917f0735d9bdf22d33f5bdb089df3f6361b0/libraries/protocol/include/hive/protocol/hive_operations.hpp#L604-619)

##### Roles: `posting active owner`

##### Parameters: `id data`

##### Example Op:

    ["custom_binary", {"id": 0, "data": ""}]
    

* * *

*   **Since: Mysterious Future**
*   **[Related](/search/?q=claim%20reward%20balance2)**

#### `claim_reward_balance2`[](#broadcast_ops_claim_reward_balance2)

Differs with original operation with extensions field and a container of tokens that will be rewarded to an account.

Note: The reward tokens are required to be unique and sorted (both by asset symbol) in ascending order. Otherwise operation validation will fail.

See: [#1859](https://archive.ph/yAE48)

##### Roles: `posting active owner`

##### Parameters: `account reward_tokens extensions`

##### Example Op:

    [
      "claim_reward_balance2",
      {
        "account": "alice",
        "reward_tokens": [
          {
            "amount": "1",
            "precision": 0,
            "nai": "@@904705667"
          }
        ],
        "extensions": []
      }
    ]
    

* * *

*   **Since: Mysterious Future**
*   **[Related](/search/?q=vote2)**

#### `vote2`[](#broadcast_ops_vote2)

This operation is used to cast a vote on a post/comment using multiple votable assets.

See: [#2748](https://archive.ph/wywr5), [SMT Voting Mana Deep Dive](https://hive.blog/smt/@vandeberg/smt-voting-mana-deep-dive)

##### Roles: `posting active owner`

##### Parameters: `voter author permlink weight extensions`

##### Example Op:

    [
      "vote2",
      {
        "voter": "hiveio",
        "author": "alice",
        "permlink": "a-post-by-alice",
        "rshares": [[{"nai": "@@904705667", "decimals": 0}, 0]],
        "extensions": []
      }
    ]
    

* * *

*   **Since: Mysterious Future**
*   **[Related](/search/?q=smt%20setup)**

#### `smt_setup`[](#broadcast_ops_smt_setup)

Setup a Smart Media Token. Each SMT has an associated descriptor object which has _permanent_ configuration data. This data cannot be changed after launch.

**Parameters:**

*   `control_account` - The name of the controlling account.
*   `symbol` - The asset symbol of the created token.
*   `max_supply` - The maximum supply of a smart media token.
*   `contribution_begin_time` - The start time of the ICO contribution process.
*   `contribution_end_time` - The end time of the ICO contribution process.
*   `launch_time` - The time in which a token should launch.
*   `hive_units_min` - The minimum HIVE units required for a successful ICO.
*   `hive_units_soft_cap` - The HIVE unit cap in which the pre\_soft\_cap\_unit generation policy applies.
*   `hive_units_hard_cap` - The HIVE unit cap in which the post\_soft\_cap\_unit generation policy applies.
*   `initial_generation_policy` - A JSON string of the HIVE and token destination routes of the ICO process.

**Example Initial Generation Policy JSON:**

    {"type": "smt_capped_generation_policy", "value": {
      "pre_soft_cap_unit": {
        "hive_unit": [["alice", 100]],
        "token_unit": [["$from", 5], ["alice", 1]]
      },
      "post_soft_cap_unit": {
        "hive_unit": [["alice", 100]],
        "token_unit": [["$from", 5], ["alice", 1]]
      },
      "min_hive_units_commitment": {
        "lower_bound": 1,
        "upper_bound": 1,
        "hash": "32edb6022c0921d99aa347e9cda5dc2db413f5574eebaaa8592234308ffebd2b"
      },
      "hard_cap_hive_units_commitment": {
        "lower_bound": "166666666666",
        "upper_bound": "166666666666",
        "hash": "93c5a6b892de788c5b54b63b91c4b692e36099b05d3af0d16d01c854723dda21"
      },
      "soft_cap_percent": 10000,
      "min_unit_ratio": 1000,
      "max_unit_ratio": 1000,
      "extensions": []
    }}
    

See [#3455](https://archive.ph/OhLDS), [SMT Setup](https://archive.is/qmlEv#smt-setup)

[Structure](https://gitlab.syncad.com/hive/hive/-/blob/e134c404b67fae7dba439162344332e369a4c269/libraries/protocol/include/steem/protocol/smt_operations.hpp#L67-L90)

##### Roles: `active owner`

##### Parameters: `control_account symbol contribution_begin_time contribution_end_time launch_time max_supply hive_units_hard_cap hive_units_soft_cap hive_units_min initial_generation_policy extensions`

##### Example Op:

    [
      "smt_setup",
      {
        "control_account": "alice",
        "symbol": {"nai": "@@000000000", "decimals": 0},
        "contribution_begin_time": "2019-08-26T11:22:39",
        "contribution_end_time": "2019-08-26T11:22:39",
        "launch_time": "2019-09-26T11:22:39",
        "max_supply": 1000000000000000,
        "hive_units_hard_cap": 10000,
        "hive_units_soft_cap": 1000,
        "hive_units_min": 0,
        "initial_generation_policy": "{\"type\":\"smt_capped_generation_policy\",\"value\":{\"pre_soft_cap_unit\":{\"hive_unit\":[[\"alice\",100]],\"token_unit\":[[\"$from\",5],[\"alice\",1]]},\"post_soft_cap_unit\":{\"hive_unit\":[[\"alice\",100]],\"token_unit\":[[\"$from\",5],[\"alice\",1]]},\"min_hive_units_commitment\":{\"lower_bound\":1,\"upper_bound\":1,\"hash\":\"32edb6022c0921d99aa347e9cda5dc2db413f5574eebaaa8592234308ffebd2b\"},\"hard_cap_hive_units_commitment\":{\"lower_bound\":\"166666666666\",\"upper_bound\":\"166666666666\",\"hash\":\"93c5a6b892de788c5b54b63b91c4b692e36099b05d3af0d16d01c854723dda21\"},\"soft_cap_percent\":10000,\"min_unit_ratio\":1000,\"max_unit_ratio\":1000,\"extensions\":[]}}",
        "extensions": []
      }
    ]
    

* * *

*   **Since: Mysterious Future**
*   **[Related](/search/?q=smt%20setup%20emissions)**

#### `smt_setup_emissions`[](#broadcast_ops_smt_setup_emissions)

Create Smart Media Token emissions (inflation).

**Parameters:**

*   `control_account` - The name of the controlling account.
*   `symbol` - The asset symbol of the created token.
*   `schedule_time` - The time the token is applicable.
*   `emissions_unit` - The emissions unit.
*   `interval_seconds` - The seconds between intervals.
*   `interval_count` - The number of intervals.
*   `lep_time` - The time of the left endpoint.
*   `rep_time` - The time of the right endpoint.
*   `lep_abs_amount` - The absolute emission amount of the left endpoint.
*   `rep_abs_amount` - The absolute emission amount of the right endpoint.
*   `lep_rel_amount_numerator` - The relative emission numerator of the left endpoint.
*   `rep_rel_amount_numerator` - The relative emission numerator of the right endpoint.
*   `rel_amount_denom_bits` - The about of bits to shift for the relative denominator.
*   `remove` - Indicates whether an emission should be added or removed.
*   `floor_emissions` - Indicates whether we should consider the lowest or highest value with regards to relative and absolute emissions.

See: [#1513](https://archive.is/3hjBC), [#2738](https://archive.ph/6sdHE), [SMT Pre-Setup](https://archive.is/qmlEv#smt-pre-setup), [Inflation Operations](https://archive.is/qmlEv#inflation-operations), [Full JSON Examples](https://archive.is/qmlEv#full-json-examples), [Inflation FAQ](https://archive.is/qmlEv#inflation-faq)

[Structure](https://gitlab.syncad.com/hive/hive/-/blob/e134c404b67fae7dba439162344332e369a4c269/libraries/protocol/include/steem/protocol/smt_operations.hpp#L100-L129)

##### Roles: `active owner`

##### Parameters: `control_account symbol emissions_unit interval_seconds interval_count lep_time rep_time lep_abs_amount rep_abs_amount lep_rel_amount_numerator rep_rel_amount_numerator rel_amount_denom_bits remove floor_emissions`

##### Example Op:

    [
      "smt_setup_emissions",
      {
        "control_account": "alice",
        "symbol": {"nai": "@@904705667", "decimals": 0},
        "schedule_time": "2019-08-26T11:22:39",
        "emissions_unit": {"token_unit": [["alice", 1]]},
        "interval_seconds": 21600,
        "interval_count": 1,
        "lep_time": "2019-08-26T11:22:39",
        "rep_time": "2019-08-26T11:22:39",
        "lep_abs_amount": {
          "amount": "1",
          "precision": 0,
          "nai": "@@904705667"
        },
        "rep_abs_amount": {
          "amount": "1",
          "precision": 0,
          "nai": "@@904705667"
        },
        "lep_rel_amount_numerator": 0,
        "rep_rel_amount_numerator": 0,
        "rel_amount_denom_bits": 0,
        "remove": false,
        "floor_emissions": false,
        "extensions": []
      }
    ]
    

* * *

*   **Since: Mysterious Future**
*   **[Related](/search/?q=smt%20set%20setup%20parameters)**

#### `smt_set_setup_parameters`[](#broadcast_ops_smt_set_setup_parameters)

Creates Smart Media Token setup parameters.

**Parameters:**

*   `control_account` - The name of the controlling account.
*   `symbol` - The asset symbol of the created token.
*   `setup_parameters` - The SMT setup parameters

See: [#2727](https://archive.ph/0kJq7), [Named Token Parameters](https://archive.is/qmlEv#named-token-parameters)

[Structure](https://gitlab.syncad.com/hive/hive/-/blob/e134c404b67fae7dba439162344332e369a4c269/libraries/protocol/include/steem/protocol/smt_operations.hpp#L172-L183)

##### Roles: `active owner`

##### Parameters: `control_account symbol setup_parameters`

##### Example Op:

    [
      "smt_set_setup_parameters",
      {
        "control_account": "alice",
        "symbol": {"nai": "@@000000000", "decimals": 0},
        "setup_parameters": [
          {
            "type": "smt_param_allow_voting",
            "value": {"value": true}
          }
        ],
        "extensions": []
      }
    ]
    

* * *

*   **Since: Mysterious Future**
*   **[Related](/search/?q=smt%20set%20runtime%20parameters)**

#### `smt_set_runtime_parameters`[](#broadcast_ops_smt_set_runtime_parameters)

Creates Smart Media Token runtime parameters.

**Parameters:**

*   `control_account` - The name of the controlling account.
*   `symbol` - The asset symbol of the created token.
*   `runtime_parameters` - The SMT runtime parameters.

**Allowed Author Reward Curves:**

*   `linear`
*   `quadratic`

**Allowed Curation Reward Curves:**

*   `linear`
*   `square_root`
*   `bounded_curation`

See: [Named Token Parameters](https://archive.is/qmlEv#named-token-parameters)

[Structure](https://gitlab.syncad.com/hive/hive/-/blob/e134c404b67fae7dba439162344332e369a4c269/libraries/protocol/include/steem/protocol/smt_operations.hpp#L185-L196)

##### Roles: `active owner`

##### Parameters: `control_account symbol runtime_parameters`

##### Example Op:

    [
      "smt_set_runtime_parameters",
      {
        "control_account": "alice",
        "symbol": {"nai": "@@000000000", "decimals": 0},
        "runtime_parameters": [
          {
            "type": "smt_param_windows_v1",
            "value": {
              "cashout_window_seconds": 90001,
              "reverse_auction_window_seconds": 110
            }
          },
          {
            "type": "smt_param_vote_regeneration_period_seconds_v1",
            "value": {
              "vote_regeneration_period_seconds": 7000,
              "votes_per_regeneration_period": 1
            }
          },
          {
            "type": "smt_param_rewards_v1",
            "value": {
              "content_constant": 9005,
              "percent_curation_rewards": 9006,
              "author_reward_curve": "quadratic",
              "curation_reward_curve": "bounded_curation"
            }
          },
          {
            "type": "smt_param_allow_downvotes",
            "value": {"value": true}
          }
        ],
        "extensions": []
      }
    ]
    

* * *

*   **Since: Mysterious Future**
*   **[Related](/search/?q=smt%20create)**

#### `smt_create`[](#broadcast_ops_smt_create)

Create a Smart Media Token.

This operation introduces new SMT into blockchain as identified by Numerical Asset Identifier (NAI). Also the SMT precision (decimal points) is explicitly provided.

#### Initial Case

The first operation to be executed is an `smt_create` operation. This operation creates an SMT object in the blockchain state. After executing this operation, the newly created SMT object is not yet fully configured.

Most of the configuration occurs in subsequent operations (`smt_set_setup_parameters`, `smt_setup_inflation`, and `smt_setup`). These later operations may occur in the same transaction, but they may also occur at any later point in time.

#### Reset Case

Re-issuing `smt_create` with zero `smt_creation_fee` and the NAI of a token in the initial setup will reset emmisions and setup state. This is useful for token creators who have put their token in an unlaunchable state.

This will allow deleting of emission schedules with and changing of precision if there are no emission objects already created.

**Parameters:**

*   `control_account` - The name of the controlling account.
*   `symbol` - The asset symbol of the created token.
*   `smt_creation_fee` - The amount to be transfered from @account to null account as elevation fee. The amount required is set by the `smt_creation_fee` field of the `dynamic_global_properties` object. This field may contain a value in HIVE or HBD.
*   `precision` - Separately provided precision for clarity and redundancy.

See: [SMT Object Creation](https://archive.is/qmlEv#smt-object-creation)

[Structure](https://gitlab.syncad.com/hive/hive/-/blob/e134c404b67fae7dba439162344332e369a4c269/libraries/protocol/include/steem/protocol/smt_operations.hpp#L16-L37)

##### Roles: `active owner`

##### Parameters: `control_account symbol smt_creation_fee precision`

##### Example Op:

    [
      "smt_create",
      {
        "control_account": "alice",
        "symbol": {"nai": "@@000000000", "decimals": 0},
        "smt_creation_fee": {
          "amount": "3000",
          "precision": 3,
          "nai": "@@000000013"
        },
        "precision": 0,
        "extensions": []
      }
    ]
    

* * *

*   **Since: Mysterious Future**
*   **[Related](/search/?q=smt%20contribute)**

#### `smt_contribute`[](#broadcast_ops_smt_contribute)

Contribute to a token ICO.

**Parameters:**

*   `contributor` The name of the contributor
*   `symbol` The asset symbol of the SMT
*   `contribution_id` A unique contribution ID number
*   `contribution` The contribution (in HIVE)

See: [#2730](https://archive.ph/iNUzf), [Token Units](https://archive.is/qmlEv#token-units)

[Structure](https://gitlab.syncad.com/hive/hive/-/blob/e134c404b67fae7dba439162344332e369a4c269/libraries/protocol/include/steem/protocol/smt_operations.hpp#L198-L209)

##### Roles: `active owner`

##### Parameters: `contributor symbol contribution_id contribution`

##### Example Op:

    [
      "smt_contribute",
      {
        "contributor": "alice",
        "symbol": {"nai": "@@422838704", "decimals": 0},
        "contribution_id": 0,
        "contribution": {
          "amount": "1000",
          "precision": 3,
          "nai": "@@000000021"
        },
        "extensions": []
      }
    ]
    

* * *

*   **Since: HF20**
*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/voclearnullaccountbalances)
    
*   **[Related](/search/?q=clear%20null%20account%20balance)**

#### `clear_null_account_balance`[](#broadcast_ops_clear_null_account_balance)

For per-block processing that clears null account balances.

See: [#2627](https://archive.ph/i4Sav), [#3556](https://archive.ph/KE2NC) (possibly planned for deprecation with SMT Hardfork, if implemented)

##### Roles: `active owner`

##### Parameters: `total_cleared`

##### Example Op:

    [
      "clear_null_account_balance",
      {
        "total_cleared": [
          {
            "amount": "3000",
            "precision": 3,
            "nai": "@@000000021"
          }
        ]
      }
    ]
    

* * *

*   **Since: HF21**
*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/voproposalpays)
    
*   **[Related](/search/?q=proposal%20pay)**

#### `proposal_pay`[](#broadcast_ops_proposal_pay)

Dedicated operation to be generated during proposal payment phase to provide info in Account History related to funds transfer.

This virtual operation is issued every hour during a proposal payment phase.

Proposals without any votes are not considered active and do not receive any payment.

If the payment of a proposal exceeds the amount of the available daily budget, it will receive a partial payment with what’s left in the daily budget.

##### Roles: `active owner`

##### Parameters: `receiver payment trx_id op_in_trx`

##### Example Op:

    [
      "proposal_pay",
      {
        "receiver": "hive.fund",
        "payment": "1.637 HBD",
        "trx_id": "0000000000000000000000000000000000000000",
        "op_in_trx": 0
      }
    ]
    

* * *

*   **Since: HF21**
*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/vospsfunds)
    
*   **[Related](/search/?q=sps%20fund)**

#### `sps_fund`[](#broadcast_ops_sps_fund)

Created once per maintenance interval to document how much HBD was added to the threasury from inflation in that maintenance interval (i.e., to track the funding of the DHF).

##### Roles: `active owner`

##### Parameters: `additional_funds`

##### Example Op:

    ["sps_fund", {"additional_funds": "71.460 HBD"}]
    

* * *

*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/vofillconvertrequests)
    
*   **[Related](/search/?q=fill%20convert%20request)**

#### `fill_convert_request`[](#broadcast_ops_fill_convert_request)

Fills when conversion requests with a conversion date before the head block time and then converts them to/from HIVE/HBD at the current median price feed history price times the premium.

##### Roles: `active owner`

##### Parameters: `owner requestid amount_in amount_out`

##### Example Op:

    [
      "fill_convert_request",
      {
        "owner": "titofit",
        "requestid": 3347004874,
        "amount_in": {
          "amount": "3770",
          "precision": 3,
          "nai": "@@000000013"
        },
        "amount_out": {
          "amount": "8849",
          "precision": 3,
          "nai": "@@000000021"
        }
      }
    ]
    

* * *

*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/voauthorrewards)
    
*   **[Related](/search/?q=author%20reward)**

#### `author_reward`[](#broadcast_ops_author_reward)

Triggered after the payout period on posts and comments.

##### Roles: `posting active owner`

##### Parameters: `author permlink hbd_payout hive_payout vesting_payout curators_vesting_payout`

##### Example Op:

    [
      "author_reward",
      {
        "author": "dianadora",
        "permlink": "actifit-dianadora-20210527t193130754z",
        "hbd_payout": {
          "amount": "11",
          "precision": 3,
          "nai": "@@000000013"
        },
        "hive_payout": {
          "amount": "0",
          "precision": 3,
          "nai": "@@000000021"
        },
        "vesting_payout": {
          "amount": "52734247",
          "precision": 6,
          "nai": "@@000000037"
        },
        "curators_vesting_payout": {
          "amount": "96051664",
          "precision": 6,
          "nai": "@@000000037"
        }
      }
    ]
    

* * *

*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/vocurationrewards)
    
*   **[Related](/search/?q=curation%20reward)**

#### `curation_reward`[](#broadcast_ops_curation_reward)

Issued by the blockchain after the payout period on posts and comments.

##### Roles: `posting active owner`

##### Parameters: `curator reward comment_author comment_permlink`

##### Example Op:

    [
      "curation_reward",
      {
        "curator": "hendrikdegrote",
        "reward": {
          "amount": "9349621710",
          "precision": 6,
          "nai": "@@000000037"
        },
        "comment_author": "crypt0",
        "comment_permlink": "metropolis-by-end-of-june-swt-token-now-trading-on-bittrex-roger-ver-offering-his-own-btc"
      }
    ]
    

* * *

*   **Since: HF17**
*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/vocommentrewards)
    
*   **[Related](/search/?q=comment%20reward)**

#### `comment_reward`[](#broadcast_ops_comment_reward)

Issued after the payout period on posts and comments.

The value of this operation is the global payout value for the post or comment. A separate virtual operation is issued for the author, the curators and the beneficiaries (see [author\_reward](/apidefinitions/#broadcast_ops_author_reward), [comment\_benefactor\_reward](/apidefinitions/#broadcast_ops_comment_benefactor_reward) and [curation\_reward](/apidefinitions/#broadcast_ops_curation_reward)).

The value is the equivalent HBD value of the payout even if no HBD will be effectively paid to the author, curators, or beneficiaries.

See: [#774](https://archive.ph/CAIjk)

##### Roles: `posting active owner`

##### Parameters: `author permlink payout author_rewards curator_payout_value beneficiary_payout_value`

##### Example Op:

    [
      "comment_reward",
      {
        "author": "karla95",
        "permlink": "blogging-challenge-13-pelicula-favorita",
        "payout": {
          "amount": "199",
          "precision": 3,
          "nai": "@@000000013"
        },
        "author_rewards": 256,
        "total_payout_value": {
          "amount": "108",
          "precision": 3,
          "nai": "@@000000013"
        },
        "curator_payout_value": {
          "amount": "90",
          "precision": 3,
          "nai": "@@000000013"
        },
        "beneficiary_payout_value": {
          "amount": "0",
          "precision": 3,
          "nai": "@@000000013"
        }
      }
    ]
    

* * *

*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/vointerests)
    
*   **[Related](/search/?q=interest)**

#### `interest`[](#broadcast_ops_interest)

Issued when interests are paid on HBD or HBD saving.

##### Roles: `active owner`

##### Parameters: `owner interest`

##### Example Op:

    [
      "interest",
      {"owner": "alice", "interest": "0.001 HBD"}
    ]
    

* * *

*   **Since: HF6**
*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/vofillvestingwithdraws)
    
*   **[Related](/search/?q=fill%20vesting%20withdraw)**

#### `fill_vesting_withdraw`[](#broadcast_ops_fill_vesting_withdraw)

Issued when each week after a user has initiated a withdrawal from VESTS to HIVE (see: [withdraw\_vesting](/apidefinitions/#broadcast_ops_withdraw_vesting)).

See: [#78](https://archive.ph/Myl5b)

##### Roles: `active owner`

##### Parameters: `from_account to_account withdrawn deposited`

##### Example Op:

    [
      "fill_vesting_withdraw",
      {
        "from_account": "alice",
        "to_account": "alice",
        "withdrawn": "0.026475 VESTS",
        "deposited": "0.710 HIVE"
      }
    ]
    

* * *

*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/vofillorders)
    
*   **[Related](/search/?q=fill%20order)**

#### `fill_order`[](#broadcast_ops_fill_order)

Issued when orders on the internal market are filled (see: [limit\_order\_create](/apidefinitions/#broadcast_ops_limit_order_create)).

##### Roles: `posting active owner`

##### Parameters: `current_owner current_orderid current_pays open_owner open_orderid open_pays`

##### Example Op:

    [
      "fill_order",
      {
        "current_owner": "alice",
        "current_orderid": 42896,
        "current_pays": "94.999 HBD",
        "open_owner": "bob",
        "open_orderid": 10001,
        "open_pays": "500.000 HIVE"
      }
    ]
    

* * *

*   **Since: HF14**
*   **Virtual Operation**
*   **Deprecated**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/voshutdownwitnesses)
    
*   **[Related](/search/?q=shutdown%20witness)**

#### `shutdown_witness`[](#broadcast_ops_shutdown_witness)

This virtual operation was previously issued when the system automatically disables a witness because it was missing too many blocks.

This operation has been introduced with HF14 and deprecated with HF20.

See: [#278](https://archive.ph/WOIVo)

##### Roles: `posting active owner`

##### Parameters: `owner`

##### Example Op:

    ["shutdown_witness", {"owner": "alice"}]
    

* * *

*   **Since: HF14**
*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/vofilltransferfromsavings)
    
*   **[Related](/search/?q=fill%20transfer%20from%20savings)**

#### `fill_transfer_from_savings`[](#broadcast_ops_fill_transfer_from_savings)

Issued when the delay for a transfer request from a savings balance is complete and the transfer is effectively executed (see: [transfer\_from\_savings](/apidefinitions/#broadcast_ops_transfer_from_savings))

##### Roles: `posting active owner`

##### Parameters: `from to amount request_id memo`

##### Example Op:

    [
      "fill_transfer_from_savings",
      {
        "from": "learngerman",
        "to": "learngerman",
        "amount": {
          "amount": "1000",
          "precision": 3,
          "nai": "@@000000021"
        },
        "request_id": 1618177172,
        "memo": ""
      }
    ]
    

* * *

*   **Since: HF9**
*   **Virtual Operation**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#get-hardfork-version)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.blockchaininstance.html#beem.blockchaininstance.BlockChainInstance.get_hardfork_properties)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.blockchaininstance.html#beem.blockchaininstance.BlockChainInstance.hardfork)
    
    [hivesql](https://docs.hivesql.io/technical-informations/database-diagram#blocks-and-transactions)
    
*   **[Related](/search/?q=hardfork)**

#### `hardfork`[](#broadcast_ops_hardfork)

Tracks hardfork activation.

Hardfork

Sheduled Hardfork Time

Actual Block

HF0

2016-03-24 16:00:00 UTC

[1](https://hiveblocks.com/b/1)

HF1

2016-04-25 17:30:00 UTC

[905693](https://hiveblocks.com/b/905693)

HF2

2016-04-26 18:00:00 UTC

[934585](https://hiveblocks.com/b/934585)

HF3

2016-04-27 13:00:00 UTC

[953363](https://hiveblocks.com/b/953363)

HF4

2016-04-30 15:00:00 UTC

[1041497](https://hiveblocks.com/b/1041497)

HF5

2016-05-31 17:00:00 UTC

[1934236](https://hiveblocks.com/b/1934236)

HF6

2016-06-30 14:00:00 UTC

[2790882](https://hiveblocks.com/b/2790882)

HF7

2016-07-04 00:00:00 UTC

[2889019](https://hiveblocks.com/b/2889019)

HF8

2016-07-04 01:00:00 UTC

[2889959](https://hiveblocks.com/b/2889959)

HF9

2016-07-14 00:00:00 UTC

[3202773](https://hiveblocks.com/b/3202773)

HF10

2016-07-15 12:00:00 UTC

[3239649](https://hiveblocks.com/b/3239649)

HF11

2016-07-17 15:00:00 UTC

[3276913](https://hiveblocks.com/b/3276913)

HF12

2016-07-26 15:00:00 UTC

[3533567](https://hiveblocks.com/b/3533567)

HF13

2016-08-15 14:00:00 UTC

[4105155](https://hiveblocks.com/b/4105155)

HF14

2016-09-20 15:00:00 UTC

[5137542](https://hiveblocks.com/b/5137542)

HF15

2016-11-08 16:00:00 UTC

[6547932](https://hiveblocks.com/b/6547932)

HF16

2016-12-06 16:00:00 UTC

[7353249](https://hiveblocks.com/b/7353249)

HF17

2017-03-30 15:00:00 UTC

[10629455](https://hiveblocks.com/b/10629455)

HF18

2017-03-30 15:00:00 UTC

[10629486](https://hiveblocks.com/b/10629486)

HF19

2017-06-20 15:00:00 UTC

[12988978](https://hiveblocks.com/b/12988978)

HF20

2018-09-25 15:00:00 UTC

[26256743](https://hiveblocks.com/b/26256743)

HF21

2019-08-27 15:00:00 UTC

[35921786](https://hiveblocks.com/b/35921786)

HF22

2019-08-29 15:00:00 UTC

[35974326](https://hiveblocks.com/b/35974326)

HF23

2020-03-20 14:00:00 UTC

[41818752](https://hiveblocks.com/b/41818752)

HF24

2020-10-06 14:00:00 UTC

[47797680](https://hiveblocks.com/b/47797680)

HF25

2021-06-30 14:00:00 UTC

[55235767](https://hiveblocks.com/b/55235767)

HF26

2022-10-11 12:00:00 UTC

[68676505](https://hiveblocks.com/b/68676505)

See: [PR2616](https://archive.is/ga0Tc), [database\_api.get\_hardfork\_properties](/apidefinitions/#database_api.get_hardfork_properties), [condenser\_api.get\_next\_scheduled\_hardfork](/apidefinitions/#condenser_api.get_next_scheduled_hardfork)

##### Roles: `posting active owner`

##### Parameters: `hardfork_id`

* * *

*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/vocommentpayoutupdates)
    
*   **[Related](/search/?q=comment%20payout%20update)**

#### `comment_payout_update`[](#broadcast_ops_comment_payout_update)

Issued when a post or comment reaches the end of the payout windows and its final payout values are computed.

##### Roles: `posting active owner`

##### Parameters: `author permlink`

##### Example Op:

    [
      "comment_payout_update",
      {
        "author": "pinmapple",
        "permlink": "pinmapple162222420235626"
      }
    ]
    

* * *

*   **Since: HF17**
*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/voreturnvestingdelegations)
    
*   **[Related](/search/?q=return%20vesting%20delegation)**

#### `return_vesting_delegation`[](#broadcast_ops_return_vesting_delegation)

Occurs when the Hive Power that has been previously delegated by an account to another account comes back to the original owner. When a user cancels its delegation, it takes 7 days to complete (see: [delegate\_vesting\_shares](/apidefinitions/#broadcast_ops_delegate_vesting_shares)).

##### Roles: `posting active owner`

##### Parameters: `account vesting_shares`

##### Example Op:

    [
      "return_vesting_delegation",
      {
        "account": "artemisha",
        "vesting_shares": {
          "amount": "18833102935",
          "precision": 6,
          "nai": "@@000000037"
        }
      }
    ]
    

* * *

*   **Since: HF17**
*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/vocommentbenefactorrewards)
    
*   **[Related](/search/?q=comment%20benefactor%20reward)**

#### `comment_benefactor_reward`[](#broadcast_ops_comment_benefactor_reward)

Triggered after the payout period on posts and comments if the original author has decided to share his reward with other users.

##### Roles: `posting active owner`

##### Parameters: `benefactor author permlink hbd_payout hive_payout vesting_payout`

##### Example Op:

    [
      "comment_benefactor_reward",
      {
        "benefactor": "hiveonboard",
        "author": "yossaeluz",
        "permlink": "importance-of-the-implementation-of-continuous-improvement-in-processes",
        "hbd_payout": {
          "amount": "40",
          "precision": 3,
          "nai": "@@000000013"
        },
        "hive_payout": {
          "amount": "0",
          "precision": 3,
          "nai": "@@000000021"
        },
        "vesting_payout": {
          "amount": "178904599",
          "precision": 6,
          "nai": "@@000000037"
        }
      }
    ]
    

* * *

*   **Since: HF17**
*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/voproducerrewards)
    
*   **[Related](/search/?q=producer%20reward)**

#### `producer_reward`[](#broadcast_ops_producer_reward)

Occurs each time a block is produced. It contains the rewards that are given to witnesses (and [previously miners](/search/?q=pow)) for their work.

Witness rewards for block signing are hard to account for. Making these rewards visible will help witnesses and prospective witnesses by providing them with more complete and accurate information to guide their decisions to invest in the platform.

##### Roles: `posting active owner`

##### Parameters: `producer vesting_shares`

##### Example Op:

    [
      "producer_reward",
      {
        "producer": "alice",
        "vesting_shares": "14403.626449 VESTS"
      }
    ]
    

* * *

*   **Since: HF23**
*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/vohardforkhives)
    
*   **[Related](/search/?q=hardfork%20hive)**

#### `hardfork_hive`[](#broadcast_ops_hardfork_hive)

At the point of the Hive hardfork, the only accounts who were not included in the initial airdrop were those containing the Steemit, Inc. ninja-mined stake and those who actively contributed to (and publicly declared support for) the centralization of the Steem Blockchain.

This virual operation tracks the initial consolidation of stake into the treasury, on the above criteria.

Also represents the moment Hive forked from the previous chain.

See: [Hive Announcement](https://peakd.com/communityfork/@hiveio/announcing-the-launch-of-hive-blockchain#will-all-steem-accounts-be-included-in-the-hive-airdrop), [Block No. 41818752](https://hiveblocks.com/b/41818752), [e9f2f73](https://gitlab.syncad.com/hive/hive/-/commit/e9f2f7302bbf691c8084383edc85d10f4aee58f9)

##### Roles: `posting active owner`

##### Parameters: `account treasury hbd_transferred hive_transferred vests_converted total_hive_from_vests`

##### Example Op:

    [
      "hardfork_hive",
      {
        "account": "steem",
        "treasury": "steem.dao",
        "hbd_transferred": {
          "amount": "861823",
          "precision": 3,
          "nai": "@@000000013"
        },
        "hive_transferred": {
          "amount": "40590",
          "precision": 3,
          "nai": "@@000000021"
        },
        "vests_converted": {
          "amount": "22870822335791719",
          "precision": 6,
          "nai": "@@000000037"
        },
        "total_hive_from_vests": {
          "amount": "11678135805",
          "precision": 3,
          "nai": "@@000000021"
        }
      }
    ]
    

* * *

*   **Since: HF24**
*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/vohardforkhiverestores)
    
*   **[Related](/search/?q=hardfork%20hive%20restore)**

#### `hardfork_hive_restore`[](#broadcast_ops_hardfork_hive_restore)

To restore the liquid balance of accounts that were not airdropped in the original Hive hardfork.

VESTS were restored in a later transaction:

[https://hiveblocks.com/tx/1d600db22fc6f9b362db36d9f0fc521b95f8894f](https://hiveblocks.com/tx/1d600db22fc6f9b362db36d9f0fc521b95f8894f)

See: [Block No. 47797680](https://hiveblocks.com/b/47797680), [!19](https://gitlab.syncad.com/hive/hive/-/merge_requests/19), [5edf4f0](https://gitlab.syncad.com/hive/hive/-/commit/5edf4f0ba04426982ba655bf83d5acd746736d49), [restore.js](https://github.com/drov0/restore-hf23-balances/blob/master/restore.js)

##### Roles:

##### Parameters:

##### Example Op:

    [
      "hardfork_hive_restore",
      {
        "account": "yellowbird",
        "treasury": "steem.dao",
        "hbd_transferred": {
          "amount": "0",
          "precision": 3,
          "nai": "@@000000013"
        },
        "hive_transferred": {
          "amount": "1280",
          "precision": 3,
          "nai": "@@000000021"
        }
      }
    ]
    

* * *

*   **Since: HF24**
*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/vodelayedvotings)
    
*   **[Related](/search/?q=delayed%20voting)**

#### `delayed_voting`[](#broadcast_ops_delayed_voting)

Tracks when newly powered up VESTS become counted towards witness and DHF proposals (after a 30 day delay is complete).

See: [transfer\_to\_vesting](/apidefinitions/#broadcast_ops_transfer_to_vesting), [fa63145](https://gitlab.syncad.com/hive/hive/-/commit/fa63145e21e008c672fbbb1ec3420b40711aa1ee), [5](https://gitlab.syncad.com/hive/hive/-/issues/5), [!21](https://gitlab.syncad.com/hive/hive/-/merge_requests/21)

##### Roles:

##### Parameters:

##### Example Op:

    [
      "delayed_voting",
      {"voter": "fordummies", "votes": 191547046}
    ]
    

* * *

*   **Since: HF24**
*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/voconsolidatetreasurybalances)
    
*   **[Related](/search/?q=consolidate%20treasury%20balance)**

#### `consolidate_treasury_balance`[](#broadcast_ops_consolidate_treasury_balance)

Tracks when balances move from old treasury account to current one, on an ongoing basis. Note that the obsolete account is still considered a treasury (cannot be reused for other purposes), but all funds and actions are redirected to new one.

For example, if an author designates the obsolete account as beneficiary, the reward will briefly exist in the obsolete account until consoldated to the new account.

See: [2074917](https://gitlab.syncad.com/hive/hive/-/commit/2074917f0735d9bdf22d33f5bdb089df3f6361b0), [`OBSOLETE_TREASURY_ACCOUNT`](/tutorials-recipes/understanding-configuration-values.html#OBSOLETE_TREASURY_ACCOUNT), [`NEW_HIVE_TREASURY_ACCOUNT`](/tutorials-recipes/understanding-configuration-values.html#NEW_HIVE_TREASURY_ACCOUNT)

##### Roles: `posting active owner`

##### Parameters: `total_moved`

##### Example Op:

    [
      "consolidate_treasury_balance",
      {
        "total_moved": [
          {
            "amount": "8853",
            "precision": 3,
            "nai": "@@000000013"
          }
        ]
      }
    ]
    

* * *

*   **Since: HF24**
*   **Virtual Operation**
*   **[Related](/search/?q=effective%20comment%20vote)**

#### `effective_comment_vote`[](#broadcast_ops_effective_comment_vote)

This virtual operation is issued when a vote on a post or comment becomes effective (see: [vote](/apidefinitions/#broadcast_ops_vote))

Needed by hivemind to index estimated `pending_payout` from a given vote.

See: [2074917](https://gitlab.syncad.com/hive/hive/-/commit/2074917f0735d9bdf22d33f5bdb089df3f6361b0)

##### Roles: `posting active owner`

##### Parameters: `voter author permlink weight rshares total_vote_weight pending_payout`

##### Example Op:

    [
      "effective_comment_vote",
      {
        "voter": "hivebuzz",
        "author": "papilloncharity",
        "permlink": "re-hivebuzz-qrevvy",
        "weight": 3658,
        "rshares": "7332260842",
        "total_vote_weight": 3658,
        "pending_payout": {
          "amount": "4",
          "precision": 3,
          "nai": "@@000000013"
        }
      }
    ]
    

* * *

*   **Since: HF24**
*   **Virtual Operation**
*   **[Related](/search/?q=ineffective%20delete%20comment)**

#### `ineffective_delete_comment`[](#broadcast_ops_ineffective_delete_comment)

Track comments that were intended to be removed but weren’t due to having a payout due to net positive votes. This operation is used to communicate to hivemind in order to avoid hiding comments with payout.

See: [!94](https://gitlab.syncad.com/hive/hive/-/merge_requests/94)

##### Roles:

##### Parameters:

* * *

*   **Since: HF24**
*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/vospsconverts)
    
*   **[Related](/search/?q=sps%20convert)**

#### `sps_convert`[](#broadcast_ops_sps_convert)

Issued when a Proposals Fund (DHF) conversion from HIVE to HBD occurs.

When the Hardfork that created Hive happened back in March 2020, the Steemit Inc ninja-mined funds were moved into the @hive.fund account as a development fund. As proposals are paid in HBD and most of the moved funds were in HIVE, an automatic conversion process has been put in place.

See: [96254ae](https://gitlab.syncad.com/hive/hive/-/commit/96254ae57c9e92cdf066e4ccd5deeed4ec9d964f)

##### Roles:

##### Parameters: `fund_account hive_amount_in hbd_amount_out`

##### Example Op:

    [
      "sps_convert",
      {
        "fund_account": "hive.fund",
        "hive_amount_in": {
          "amount": "37111024",
          "precision": 3,
          "nai": "@@000000021"
        },
        "hbd_amount_out": {
          "amount": "15735074",
          "precision": 3,
          "nai": "@@000000013"
        }
      }
    ]
    

* * *

*   **Since: HF25**
*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/voaccountcreateds-hf25)
    
*   **[Related](/search/?q=account%20created)**

#### `account_created`[](#broadcast_ops_account_created)

Issued each time a new account has been successfully created.

##### Roles:

##### Parameters: `new_account_name creator initial_vesting_shares initial_delegation`

##### Example Op:

    [
      "account_created",
      {
        "new_account_name": "init-2",
        "creator": "initminer",
        "initial_vesting_shares": {
          "amount": "0",
          "precision": 6,
          "nai": "@@000000037"
        },
        "initial_delegation": {
          "amount": "0",
          "precision": 6,
          "nai": "@@000000037"
        }
      }
    ]
    

* * *

*   **Since: HF25**
*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/vochangedrecoveryaccounts-hf25)
    
*   **[Related](/search/?q=changed%20recovery%20account)**

#### `changed_recovery_account`[](#broadcast_ops_changed_recovery_account)

Issued when the blockchain effectively changes the recovery account of an account after it issued such request (see: [change\_recovery\_account](/apidefinitions/#broadcast_ops_change_recovery_account)).

##### Roles:

##### Parameters: `account old_recovery_account new_recovery_account`

##### Example Op:

    [
      "changed_recovery_account",
      {
        "account": "alice",
        "old_recovery_account": "eve",
        "new_recovery_account": "bob"
      }
    ]
    

* * *

*   **Since: HF25**
*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/voexpiredaccountnotifications-hf25)
    
*   **[Related](/search/?q=expired%20account%20notification)**

#### `expired_account_notification`[](#broadcast_ops_expired_account_notification)

Issued when governance votes for an account have expired and are removed.

##### Roles:

##### Parameters: `account`

##### Example Op:

    [
      "expired_account_notification",
      {"account": "init-2"}
    ]
    

* * *

*   **Since: HF25**
*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/vofailedrecurrenttransfers-hf25)
    
*   **[Related](/search/?q=failed%20recurrent%20transfer)**

#### `failed_recurrent_transfer`[](#broadcast_ops_failed_recurrent_transfer)

Issued when a recurrent transfer has failed to be executed (see: [recurrent\_transfer](/apidefinitions/#broadcast_ops_recurrent_transfer)).

##### Roles:

##### Parameters: `from to amount memo consecutive_failures remaining_executions deleted`

* * *

*   **Since: HF25**
*   **Virtual Operation**
*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/-/blob/master/doc/README.md#collateralized-convert)
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/vofillcollateralizedconvertrequests-hf25)
    
*   **[Related](/search/?q=fill%20collateralized%20convert%20request)**

#### `fill_collateralized_convert_request`[](#broadcast_ops_fill_collateralized_convert_request)

Issued when a HIVE to HBD conversion is completed (see: [recurrent\_transfer](/apidefinitions/#broadcast_ops_collateralized_convert)).

##### Roles:

##### Parameters: `owner requestid amount_in amount_out excess_collateral`

* * *

*   **Since: HF25**
*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/vofillrecurrenttransfers-hf25)
    
*   **[Related](/search/?q=fill%20recurrent%20transfer)**

#### `fill_recurrent_transfer`[](#broadcast_ops_fill_recurrent_transfer)

Issued when a recurrent transfer is executed (see: [recurrent\_transfer](/apidefinitions/#broadcast_ops_recurrent_transfer)).

##### Roles:

##### Parameters: `from to amount memo remaining_executions`

* * *

*   **Since: HF25**
*   **Virtual Operation**
*   **SDK Reference**
    
    [hivesql](https://docs.hivesql.io/technical-informations/virtual-operations/vofillrecurrenttransfers-hf25)
    
*   **[Related](/search/?q=transfer%20to%20vesting%20completed)**

#### `transfer_to_vesting_completed`[](#broadcast_ops_transfer_to_vesting_completed)

Issued when a power-up is finally taken into account for governance votes (see: [transfer\_to\_vesting](/apidefinitions/#broadcast_ops_transfer_to_vesting)).

See: [#111](https://gitlab.syncad.com/hive/hive/-/issues/111)

##### Roles:

##### Parameters: `from_account to_account hive_vested vesting_shares_received`

* * *

### Broadcast OPS Custom

Ops:

*   [flagPost](#broadcast_ops_customs_flagPost)
*   [mutePost](#broadcast_ops_customs_mutePost)
*   [pinPost](#broadcast_ops_customs_pinPost)
*   [setRole](#broadcast_ops_customs_setRole)
*   [setUserTitle](#broadcast_ops_customs_setUserTitle)
*   [subscribe](#broadcast_ops_customs_subscribe)
*   [unmutePost](#broadcast_ops_customs_unmutePost)
*   [unpinPost](#broadcast_ops_customs_unpinPost)
*   [unsubscribe](#broadcast_ops_customs_unsubscribe)
*   [updateProps](#broadcast_ops_customs_updateProps)

To interact with the communities framework, use `custom_json` operations with the an `id` of `community`. Communities also intepret other ids like `follow` and `reblog`.

See: [communities.md](https://gitlab.syncad.com/hive/hivemind/-/blob/master/docs/communities.md)

Also see: [Bridge](/apidefinitions/#apidefinitions-bridge), [Broadcast Transaction](/apidefinitions/#condenser_api.broadcast_transaction), [`custom_json`](/apidefinitions/#broadcast_ops_custom_json)

*   **SDK Reference**
    
    [hive-keychain](https://github.com/stoodkev/hive-keychain#requestcustomjson)
    
    [hivesigner.js](https://github.com/ecency/hivesigner-sdk#custom-json)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#custom-json)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.custom_json)
    
*   **[Related](/search/?q=setrole)**

#### `setRole`[](#broadcast_ops_customs_setRole)

Sets a role for a given account in a community.

*   _Owner_ can set any role.
*   _Admins_ can set the role of any account to any level below `admin`, except for other _Admins_.
*   _Mods_ can set the role of any account to any level below `mod`, except for other _Mods_.

##### Roles: `posting`

##### Parameters: `community account role`

##### Example Op:

    [
      "custom_json",
      {
        "required_auths": [],
        "required_posting_auths": ["alice"],
        "id": "community",
        "json": "[\"setRole\", {\"community\": \"hive-123456\", \"account\": \"bob\", \"role\": \"admin\"}]"
      }
    ]
    

    [
      "custom_json",
      {
        "required_auths": [],
        "required_posting_auths": ["alice"],
        "id": "community",
        "json": "[\"setRole\", {\"community\": \"hive-123456\", \"account\": \"charlie\", \"role\": \"mod\"}]"
      }
    ]
    

    [
      "custom_json",
      {
        "required_auths": [],
        "required_posting_auths": ["alice"],
        "id": "community",
        "json": "[\"setRole\", {\"community\": \"hive-123456\", \"account\": \"dave\", \"role\": \"guest\"}]"
      }
    ]
    

    [
      "custom_json",
      {
        "required_auths": [],
        "required_posting_auths": ["alice"],
        "id": "community",
        "json": "[\"setRole\", {\"community\": \"hive-123456\", \"account\": \"edward\", \"role\": \"member\"}]"
      }
    ]
    

* * *

*   **SDK Reference**
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#custom-json)
    
    [hivesigner.js](https://github.com/ecency/hivesigner-sdk#custom-json)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.custom_json)
    
*   **[Related](/search/?q=setusertitle)**

#### `setUserTitle`[](#broadcast_ops_customs_setUserTitle)

Sets a title (badge) for a given account in a community (_Mods_ or higher).

##### Roles: `posting`

##### Parameters: `community account title`

##### Example Op:

    [
      "custom_json",
      {
        "required_auths": [],
        "required_posting_auths": ["alice"],
        "id": "community",
        "json": "[\"setUserTitle\", {\"community\": \"hive-123456\", \"account\": \"alice\", \"title\": \"Founder\"}]"
      }
    ]
    

* * *

*   **SDK Reference**
    
    [hive-keychain](https://github.com/stoodkev/hive-keychain#requestcustomjson)
    
    [hivesigner.js](https://github.com/ecency/hivesigner-sdk#custom-json)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#custom-json)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.custom_json)
    
*   **[Related](/search/?q=mutepost)**

#### `mutePost`[](#broadcast_ops_customs_mutePost)

Mute a post (_Mods_ or higher). Can be a topic or a comment.

**Note:** Any posts muted for spam should contain simply the string spam in the notes field. This standardized label will help train automated spam detection.

##### Roles:

##### Parameters:

##### Example Op:

    [
      "custom_json",
      {
        "required_auths": [],
        "required_posting_auths": ["alice"],
        "id": "community",
        "json": "[\"mutePost\",{\"community\":\"hive-123456\",\"account\":\"eve\",\"permlink\":\"re-eve-comment-1564339652z\",\"notes\":\"Off Topic\"}]"
      }
    ]
    

* * *

*   **SDK Reference**
    
    [hive-keychain](https://github.com/stoodkev/hive-keychain#requestcustomjson)
    
    [hivesigner.js](https://github.com/ecency/hivesigner-sdk#custom-json)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#custom-json)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.custom_json)
    
*   **[Related](/search/?q=unmutepost)**

#### `unmutePost`[](#broadcast_ops_customs_unmutePost)

Unmute a post (_Mods_ or higher).

##### Roles:

##### Parameters:

##### Example Op:

    [
      "custom_json",
      {
        "required_auths": [],
        "required_posting_auths": ["alice"],
        "id": "community",
        "json": "[\"unmutePost\",{\"community\":\"hive-123456\",\"account\":\"eve\",\"permlink\":\"re-eve-comment-1564339652z\",\"notes\":\"On Topic (on second thought)\"}]"
      }
    ]
    

* * *

*   **SDK Reference**
    
    [hive-keychain](https://github.com/stoodkev/hive-keychain#requestcustomjson)
    
    [hivesigner.js](https://github.com/ecency/hivesigner-sdk#custom-json)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#custom-json)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.custom_json)
    
*   **[Related](/search/?q=updateprops)**

#### `updateProps`[](#broadcast_ops_customs_updateProps)

##### Roles:

##### Parameters:

##### Example Op:

    [
      "custom_json",
      {
        "required_auths": [],
        "required_posting_auths": ["alice"],
        "id": "community",
        "json": "[\"updateProps\",{\"community\":\"hive-123456\",\"props\":{\"title\":\"Anti-Knitting\",\"about\":\"A community against knitting.\",\"is_nsfw\":false,\"description\":\"If you like to knitting, go away.\",\"flag_text\":\"Must hate knitting or else you will be muted.\"}}]"
      }
    ]
    

* * *

*   **SDK Reference**
    
    [hive-keychain](https://github.com/stoodkev/hive-keychain#requestcustomjson)
    
    [hivesigner.js](https://github.com/ecency/hivesigner-sdk#custom-json)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#custom-json)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.custom_json)
    
*   **[Related](/search/?q=subscribe)**

#### `subscribe`[](#broadcast_ops_customs_subscribe)

Allows a user to signify they want this community shown on their personal trending feed and to be shown in their navigation menu.

##### Roles:

##### Parameters:

##### Example Op:

    [
      "custom_json",
      {
        "required_auths": [],
        "required_posting_auths": ["alice"],
        "id": "community",
        "json": "[\"subscribe\",{\"community\":\"hive-123456\"}]"
      }
    ]
    

* * *

*   **SDK Reference**
    
    [hive-keychain](https://github.com/stoodkev/hive-keychain#requestcustomjson)
    
    [hivesigner.js](https://github.com/ecency/hivesigner-sdk#custom-json)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#custom-json)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.custom_json)
    
*   **[Related](/search/?q=pinpost)**

#### `pinPost`[](#broadcast_ops_customs_pinPost)

Stickies a post to the top of the community homepage (_Mods_ or higher). If multiple posts are stickied, the newest ones are shown first.

##### Roles:

##### Parameters:

##### Example Op:

    [
      "custom_json",
      {
        "required_auths": [],
        "required_posting_auths": ["alice"],
        "id": "community",
        "json": "[\"pinPost\",{\"community\":\"hive-123456\",\"account\":\"alice\",\"permlink\":\"a-post-by-alice\"}]"
      }
    ]
    

* * *

*   **SDK Reference**
    
    [hive-keychain](https://github.com/stoodkev/hive-keychain#requestcustomjson)
    
    [hivesigner.js](https://github.com/ecency/hivesigner-sdk#custom-json)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#custom-json)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.custom_json)
    
*   **[Related](/search/?q=unsubscribe)**

#### `unsubscribe`[](#broadcast_ops_customs_unsubscribe)

Allows a user to signify they no longer want this community shown on their personal trending feed or to be shown in their navigation menu.

##### Roles:

##### Parameters:

##### Example Op:

    [
      "custom_json",
      {
        "required_auths": [],
        "required_posting_auths": ["alice"],
        "id": "community",
        "json": "[\"unsubscribe\",{\"community\":\"hive-123456\"}]"
      }
    ]
    

* * *

*   **SDK Reference**
    
    [hive-keychain](https://github.com/stoodkev/hive-keychain#requestcustomjson)
    
    [hivesigner.js](https://github.com/ecency/hivesigner-sdk#custom-json)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#custom-json)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.custom_json)
    
*   **[Related](/search/?q=unpinpost)**

#### `unpinPost`[](#broadcast_ops_customs_unpinPost)

Removes a post to the top of the community homepage (_Mods_ or higher).

##### Roles:

##### Parameters:

##### Example Op:

    [
      "custom_json",
      {
        "required_auths": [],
        "required_posting_auths": ["alice"],
        "id": "community",
        "json": "[\"unpinPost\",{\"community\":\"hive-123456\",\"account\":\"alice\",\"permlink\":\"a-post-by-alice\"}]"
      }
    ]
    

* * *

*   **SDK Reference**
    
    [hive-keychain](https://github.com/stoodkev/hive-keychain#requestcustomjson)
    
    [hivesigner.js](https://github.com/ecency/hivesigner-sdk#custom-json)
    
    [hive-js](https://gitlab.syncad.com/hive/hive-js/tree/master/doc#custom-json)
    
    [beem](https://beem.readthedocs.io/en/latest/beem.transactionbuilder.html)
    
    [hive-ruby](https://www.rubydoc.info/gems/hive-ruby/Hive/Broadcast.custom_json)
    
*   **[Related](/search/?q=flagpost)**

#### `flagPost`[](#broadcast_ops_customs_flagPost)

Used by guests to suggest a post for the review queue. It’s up to the community to define what constitutes flagging.

##### Roles:

##### Parameters:

##### Example Op:

    [
      "custom_json",
      {
        "required_auths": [],
        "required_posting_auths": ["alice"],
        "id": "community",
        "json": "[\"flagPost\",{\"community\":\"hive-123456\",\"account\":\"eve\",\"permlink\":\"a-post-by-eve\",\"notes\":\"Warning\"}]"
      }
    ]
    

* * *

[Back to top](#)
