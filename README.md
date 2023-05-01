Download Link: https://assignmentchef.com/product/solved-blockchain-homework-5
<br>
<ul>

 <li>The term “mainnet” refers to the actual Bitcoin blockchain network. The term “testnet” is an alternative to mainnet to be used for testing. Testnet coins are separate and distinct from actual bitcoins, and are never supposed to have any value. This allows application developers or bitcoin testers to experiment, without having to use real bitcoins or worrying about breaking the main bitcoin chain. You can obtain testnet coins for free from the faucet at <a href="https://testnet.coinfaucet.eu/en/">https://testnet.coinfaucet.eu/en/</a><a href="https://testnet.coinfaucet.eu/en/">.</a> It is courteous to send the testnet coins back to the faucet after you are done experimenting with them.</li>

</ul>




<ol>

 <li>Read:

  <ol>

   <li>Bitcoin addresses:

    <ol>

     <li><a href="https://en.bitcoin.it/wiki/Address">https://en.bitcoin.it/wiki/Address</a></li>

     <li><a href="https://en.bitcoin.it/wiki/Technical_background_of_version_1_Bitcoin_addresses">https://en.bitcoin.it/wiki/Technical_background_of_version_1_Bitcoin_addresses</a></li>

    </ol></li>

  </ol></li>

</ol>

<ul>

 <li><a href="https://en.bitcoin.it/wiki/List_of_address_prefixes">https://en.bitcoin.it/wiki/List_of_address_prefixes</a></li>

</ul>

<ol>

 <li>Base58 encoding: <a href="https://en.bitcoin.it/wiki/Base58Check_encoding">https://en.bitcoin.it/wiki/Base58Check_encoding</a></li>

 <li>Bitcoin address reuse and privacy: <a href="https://en.bitcoin.it/wiki/Address_reuse">https://en.bitcoin.it/wiki/Address_reuse</a></li>

 <li>Testnet: <a href="https://en.bitcoin.it/wiki/Testnet">https://en.bitcoin.it/wiki/Testnet</a></li>

 <li>BitcoinJ

  <ol>

   <li><a href="https://bitcoinj.github.io/#getting-started">https://bitcoinj.github.io/#getting</a><a href="https://bitcoinj.github.io/#getting-started">–</a><a href="https://bitcoinj.github.io/#getting-started">started</a></li>

   <li><a href="https://bitcoinj.github.io/working-with-transactions">https://bitcoinj.github.io/working</a><a href="https://bitcoinj.github.io/working-with-transactions">–</a><a href="https://bitcoinj.github.io/working-with-transactions">with</a><a href="https://bitcoinj.github.io/working-with-transactions">–</a><a href="https://bitcoinj.github.io/working-with-transactions">transactions</a> <a href="https://bitcoinj.github.io/working-with-the-wallet">https://bitcoinj.github.io/working</a><a href="https://bitcoinj.github.io/working-with-the-wallet">–</a><a href="https://bitcoinj.github.io/working-with-the-wallet">with</a><a href="https://bitcoinj.github.io/working-with-the-wallet">–</a><a href="https://bitcoinj.github.io/working-with-the-wallet">the</a><a href="https://bitcoinj.github.io/working-with-the-wallet">–</a><a href="https://bitcoinj.github.io/working-with-the-wallet">wallet</a></li>

  </ol></li>

 <li>Set the hw5.WalletInit.WALLETS_DIR constant to a directory that stores all the wallets.</li>

 <li>Read and thoroughly understand hw5.WalletInit.</li>

 <li>Run the hw5.WalletInitTest class to create a wallet on testnet. This class will download and sync the testnet block chain on to your computer and thus may take a few minutes. Skim through the logging output to get a basic understanding of what’s happening. Submit the current receive address of your wallet as your solution to question 4 in a text file called homework5solutions.txt.</li>

 <li>Use the testnet faucet to send testnet coins to the testnet wallet’s receive address. Look up the transaction ID at the testnet blockchain explorer at <a href="https://www.blocktrail.com/tBTC">https://www.blocktrail.com/tBTC</a> to see if the transaction was submitted to the network. Be sure to receive at least one confirmation in case a double-spend attack prevented you from receiving the coins. The faucet may send the same coin to you in multiple different transactions, so the blockchain explorer may tell you that the coin has been double-spent. To find the actual transaction that successfully sent you coins, run the WalletInitTest and watch the WalletInitTest.monitor method’s periodic reporting of the transactions it receives from its peers. The output will tell you which transaction succeeded and which is dead. Submit the transaction ID and the amount of testnet coins sent to your receive address as your solution to question 5 in homework5solutions.txt. Answer the following questions: how many outputs does the transaction have? What is the purpose of the output that locks coins to the address that’s not yours?</li>

 <li>Run the hw5.WalletInitTest class again to update your wallet’s blockchain and confirm that it contains the amount given to you in question 3.</li>

 <li>Use BitcoinJ to write a custom Bitcoin address generator for mainnet. Place your implementation in the method CustomAddressGenerator.get(String). This method has one parameter which is a string called prefix encoded in base58. The method returns a bitcoin address on mainnet that begins with 1 followed by prefix. Submit your CustomAddressGenerator class.</li>

 <li>Use the CustomAddressGenerator.get(String) method to generate a mainnet address that begins with 1 followed by the first four letters of your last name in uppercase. If your last name is shorter than four letters, append as many “X” characters as necessary. If the first four letters of your last name in uppercase includes a letter not allowed in a Bitcoin address, then use “X” instead of the letter. Submit your custom bitcoin address as your solution to question 8 in a text file called homework5solutions.txt.</li>

</ol>