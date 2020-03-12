## How to use

1. Modify `./mainnet/mainnet.conf` file with list of your servers (remove YOUR_WSS_SERVER_4)
2. Run `docker-compose up -d`
3. Test via
`wscat -c ws://example.com:8011 -x '{"jsonrpc":"2.0","method":"eth_getBlockByNumber","params":["latest", false],"id":1}' | jq '.result.number'`