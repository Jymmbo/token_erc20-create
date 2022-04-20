# Nola sortu ERC-20 token bat

Ondorengo proiektu honetan, ERC-20 token bat sortzeko pausoak azalduko dira. Horretarako, Smart Contract bat Ethereumeko Ropsten Testnet sarean hedatuko dugu.


## Aurrekariak: Metamasken instalazioa

Edozein Blockchain sare edo DLT sistemarekin lan egiteko baldintza bi bete behar dira nagusiki. Denan den, gure kasuan, bada hirugarren bat ere:
1. Konektatu nahi dugun Blockchain sareko nodo batera konexioa izatea.
2. Gure kontu eta klabe propioak izatea, egin nahi ditugun operazio ezberdinak exekutatu ahal izateko.
3. Gure kasuan, Ethereum sare batera konektatu eta eragiketak egin ahal izateko, token kopuru nahikoa izan beharko dugu.

Guzti horretarako Metamask tresna ezin hobea da. Gure nabigatzailean instalatu dezakegun tresna bat da eta, aurreko baldintza biak betetzen laguntzen digu.

Behin Metamask instalatuta, lehendabiziko baldintza biak beteko digutu. Hala ere, dagokion Blockchain sarean eragiketak egin ahal izateko Ether (ETH) token nahiko izan beharko dugu. Ezin baitezakegu ahaztu eragiketa bakoitza ordaindu egin behar dela.

* Abibide honetan, Ethereumeko Ropsten Test sarea erabiliko dugu. Etherrak eskuratzeko, Metamask bidez Ropsten sarera konektatu eta, ageri zaigun kontuaren **helbidea** (Account) hartuko dugu. Helbide hori [Faucet](https://faucet.dimensions.network/) batean kopiatu eta, Etherren eskaera egingo dugu. Horrela, eragiketak egiteko saldo nahikoa lortuko dugu irudi honetan ageri den bezala.

![Metamask Ropsten Test Sarera konektuta eta hola eskuratu gure Helbidea](/images/metamask.png)

****************

 ## Pausoz pauso

 ### ERC20aren Smart Contractaren sorrera

 Lehendabizi, [OpenZeppelinen Wizarda](https://wizard.openzeppelin.com/) zabalduko dugu gure nabigatzailean. Bertan, ondorengo pausoak gauzatu beharko ditugu:
 * ERC20 aukera aukeratu ezkerreko menuko goikaldean.
 * ERC20 horren ezaugarriak aukeratu. Horien artean, bereziki kontuan hartu beharrekoak:
   - Name: gure tokenaren izena.
   - Symbol: gure tokenaren ikurra
   - Premint: sortuko den kopurua. Kontuan eduki berez 18 dezimal izango dituela beraz, 1 kopurua jarrita ere nahikoa litzateke. 
 * Goi-eskumako menuan, "Open in Remix" aukera sakatu.

Hona hemen adibide bat. Aurreko pausoak, gure nabigatzailean fitxa berri bat irekiko digu, **Remix** garapenerako ingurenearena. Bertan, zuzenean, gure ERC20 Smart Contracta ageriko zaigu.

![Open Zeppelineko Wizarda nola erabili adibidea](/images/oz_wizard.png)

****************


 ### Smart Contractaren hedapena Blockhain sarean

 Behin [Remixen](https://remix.ethereum.org/) gaudela, lehendabizi Smart Contractaren konpilazioa burutu beharko dugu. Horretarako, **Compile contract** botoia sakatu beharko dugu.

 Behin Smart Contracta ongi konpilatuta, ondorengo pausoak burutu beharko ditugu, hurrengo irudian ageri den bezala:
 * Remixen ezkerreko menuan **_Deploy & run transactions_** aukera aukeratuko dugu.
 * **_Environment_** aukeran _Injected Web3_ aukera aukeratu eta, Remix ingurunea gure Metamaskeko instantziara konektatuko da.
 * Smart Contractari jarri nahi dizkiogun _izena_ eta _ikurra_ aldatu.
 * **_Deploy_** botoiari eman eta, gure ERC20 tokenan hedatu arte itxaron besterik ez da geratuko.

![Remix bidez nola sortu ERC20 token bat](/images/remix.png)

****************

 ### Nola erabili gure ERC20 tokena

 Hurrengo atal honetan, ERC20 tokena Metamask bidez nola erabili azalduko dugu. Remix bidez erabili badezakegu ere, Metamaskekin nola erabili azaltzen da ondorengo pausoetan:
 * Behin gure ERC20 tokena sortu dugula, Smart Contracta hedatuz, Remixek berak Smart Contractaren helbidea emango digu. Helbide hau kopiatu beharko dugu, hurrengo irudian ageri den bezala.

 ![ERC20 tokena eskuratu, Smart Contractaren helbidearen bidez](/images/remix1.png)

 * Behin Smart Contractraren helbidea kopiatuta, Metamask zabaldu eta **"Import tokens"** aukera sakatu.
 * Ondoren, gure tokenen artean ageriko zaigu sortu berri dugu ERC20 tokena.

![Metamasken nola inportatu gure ERC20 tokena](/images/metamask1.png)
