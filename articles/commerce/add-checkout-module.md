---
title: Kassamoduuli
description: Tässä ohjeaiheessa kuvataan, miten kassamoduuli lisätään sivulle ja miten pakolliset ominaisuudet määritetään.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4b810441fd25d41ee0893b119b4f7d91e7435d21
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697080"
---
# <a name="checkout-module"></a>Kassamoduuli

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kuvataan, miten kassamoduuli lisätään sivulle ja miten pakolliset ominaisuudet määritetään.

## <a name="overview"></a>Yleiskatsaus

Kassamoduuli on erityinen säilö, joka isännöi kaikkia sellaisia moduuleja, jotka tarvitaan tilauksen luomista varten. Kassamoduuli voi sisältää moduuleja, jotka käsittelevät toimitusosoitetta, toimitusmenetelmiä, laskutustietoja, tilauksen yhteenvetoa ja muita asiakastilaukseen liittyviä tietoja. Se sisältää vaiheittaisen työnkulun, jota käyttämällä asiakas syöttää kaikki tarvittavat tiedot ostoa varten.

Kassamoduuli hahmontaa tiedot ostoskorin tunnuksen mukaan. Tämä ostoskorin tunnus tallennetaan selaimen evästeeksi. Ostoskorin tunnus on pakollinen, jotta kassamoduulin tiedot kuten tilauksen nimikkeet, kokonaissumma ja alennukset, voidaan hahmontaa.

## <a name="checkout-module-properties"></a>Kassamoduulin ominaisuudet

Kassamoduulin sisällä on moduulijoukko, jota se isännöi. Leveysominaisuuden avulla voit määrittää, tuleeko kassamoduulin nimikkeiden olla moduulin vai näytön levyisiä.

Kassamoduulissa on useita paikkoja, kuten **Kassatiedot**-, **Tilauksen yhteenveto**- ja **Tee tilaus** -paikka. Kukin paikka tukee moduulijoukkoa, joka näkyy sivun tietyssä asettelussa. Esimerkiksi **Kassatiedot**-paikka sisältää kaikki moduulit, joita tarvitaan kassatoiminnon käynnistämiseen. Näitä ovat esimerkiksi toimitusosoitteen ja maksutavan moduulit. **Tilauksen yhteenveto** -paikka näyttää tilauksen yhteenvedon ja tukee tilauksen tekemistä. **Tee tilaus** -paikka tukee myös tilauksen tekemistä. Tee tilaus -moduulit voidaan määrittää kahdessa paikassa, jotta tilausprosessi voidaan optimoida eri ympäristöissä.

### <a name="modules-that-can-be-used-in-the-checkout-module"></a>Moduulit, joita voidaan käyttää kassamoduulissa

- **Toimitusosoite** – Tämän moduulin avulla asiakas voi lisätä tai valita tilauksen toimitusosoitteen. Jos asiakas on kirjautunut sisään, kaikki kyseiselle asiakkaalle aiemmin tallennetut osoitteet näytetään. Asiakas voi valita näistä osoitteista. Asiakas voi myös lisätä uuden osoitteen. Toimitusosoitetta käytetään kaikissa tilauksen nimikkeissä, jotka edellyttävät toimitusta. Sitä ei voi mukauttaa yksittäisille rivinimikkeille. Toimitusosoitteen muodot määritetään kullekin maalle tai alueelle. Maa-/aluekohtaiset säännöt tulevat voimaan tässä moduulissa. Vaikka tämä moduuli ei sisällä osoitteen vahvistusta, osoitteen tarkistus voidaan toteuttaa mukautuksen avulla. Jos tilauksessa on vain myymälästä noudettavia nimikkeitä, tämä moduuli piilotetaan automaattisesti.
- **Toimitusvaihtoehdot** – Tämän moduulin avulla asiakas voi valita tilauksen toimitusvaihtoehdon. Toimitusvaihtoehdot perustuvat toimitusosoitteeseen. Jos toimitusosoitetta muutetaan, toimitusvaihtoehdot on noudettava uudelleen. Jos tilauksessa on vain myymälästä noudettavia nimikkeitä, tämä moduuli piilotetaan automaattisesti.
- **Kassa-osan säilö** – Tämä moduuli on säilö, jonka sisään asetetaan useita moduuleja. Ne luovat osan kassatyönkulun sisälle. Tähän säilöön voi asettaa esimerkiksi kaikki maksuun liittyvät moduulit, jolloin ne näkyvät yhtenä osana. Tämä moduuli vaikuttaa vain työnkulun asetteluun.
- **Lahjakortti** – Tämän moduulin avulla asiakas voi maksaa tilauksen käyttämällä lahjakorttia. Tämä tukee vain Microsoft Dynamics 365 Commercen lahjakortteja. Tilaukseen voi käyttää yhtä tai useaa lahjakorttia. Jos lahjakortin saldo ei kata ostoskorin summaa, lahjakortti voidaan yhdistää toiseen maksutapaan. Lahjakortteja voi lunastaa vain, jos asiakas on kirjautunut sisään.
- **Kanta-asiakkuuspisteet** – Tämän moduulin avulla asiakas voi maksaa tilauksen käyttämällä kanta-asiakkuuspisteitä. Se sisältää yhteenvedon käytettävissä olevista ja vanhenevista pisteistä. Sen avulla asiakas voi valita lunastettavien pisteiden määrän. Jos asiakas ei ole kirjautunut sisään tai ei ole kanta-asiakasohjelman jäsen tai jos ostoskorin kokonaissumma on 0 (nolla), tämä moduuli piilotetaan automaattisesti.
- **Luottokortti** – Tämän moduulin avulla asiakas voi maksaa tilauksen käyttämällä luottokorttia. Jos ostoskorin kokonaissumma katetaan kanta-asiakkuuspisteillä tai lahjakortilla tai jos summa on 0 (nolla), tämä moduuli piilotetaan automaattisesti. Luottokortin integroinnin tarjoaa Adyen-maksuyhdistin. Lisätietoja tämän yhdistimen käyttämisestä on kohdassa [Adyen-maksuyhdistin](https://).
- **Laskutusosoite** – Tämän moduulin avulla asiakas voi antaa laskutustiedot. Adyen käsittelee nämä tiedot yhdessä luottokorttitietojen kanssa. Tämä moduuli sisältää vaihtoehdon, jonka avulla asiakkaat voivat käyttää laskutusosoitetta toimitusosoitteena.
- **Yhteystiedot** – Tämän moduulin avulla asiakas voi lisätä tai muuttaa tilauksen yhteystietoja (sähköpostiosoitetta).
- **Tee tilaus** – Tämän moduulin avulla asiakas voi tehdä tilauksen.
- **Sisällöntäyteinen lohko** – Tämä moduuli sisältää kaiken viestinnän, jota sisällönhallintajärjestelmä (CMS) ohjaa. Viestintää voi olla esimerkiksi seuraava viesti: Jos tilaamisessa on ongelmia, soita numeroon 1-800-FABRIKAM. 
- **Tilauksen yhteenveto** – Tämä moduuli näyttää tilauksen kustannuserittelyn.
- **Tilausrivin nimikkeet** – Tämä moduuli näyttää yhteenvedon nimikkeistä, jotka sisällytetään tilaukseen.

## <a name="retail-server-interaction"></a>Vähittäismyynnin palvelimen vuorovaikutus

Useimmat kassatiedot, kuten toimitusosoite ja toimitustapa, tallennetaan ostoskoriin. Niitä käsitellään tilauksen osana. Ainoa poikkeus on luottokorttitiedot. Nämä tiedot käsitellään suoraan Adyen-maksuyhdistimen avulla. Maksu on vahvistettu, mutta sitä ei ole veloitettu.

## <a name="add-a-checkout-module-to-a-new-page-and-set-the-required-properties"></a>Lisää kassamoduuli uudelle sivulle ja määritä pakolliset ominaisuudet.

Voit lisätä kassamoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Siirry kohtaan **Osa \> Uusi osa** ja anna uudelle osalle nimeksi **Kassan osa**.
1. Lisää osaan kassamoduuli.
1. Lisää kassamoduuliin otsikko.
1. Lisää **Kassatiedot**-osaan toimitusosoite, toimitusvaihtoehdot, kassan osan säilö- ja yhteystietomoduulit. **Kassatiedot**-paikassa tulisi nyt olla neljä osaa.
1. Lisää kassan osan säilön moduuliin lahjakortin, kanta-asiakkuuspisteiden ja luottokortin moduulit. Tällä tavoin varmistat, että kaikki maksutavat näkyvät yhdessä osassa.
1. Lisää **Tilausyhteenveto**-paikkaan tilauksen yhteenvedon, tilauksen tekemisen ja sisällöntäyteisen lohkon moduulit.
1. Lisää sisällöntäyteisen lohkon moduuliin seuraava teksti: **Saat lisätietoja tilauksesta soittamalla numeroon 1-800-FABRIKAM.**
1. Lisää **Tee tilaus** -paikkaan tilauksen tekemisen moduuli.
1. Valitse **Tallenna**. Joitakin moduuleista ei ehkä hahmonneta esikatselussa. Tämä johtuu siitä, että niillä ei ole ostoskorin kontekstia.
1. Kirjaa osa sisään ja julkaise se.
1. Luo malli, joka käyttää uutta kassaosaa.
1. Luo kassasivu, joka käyttää uutta mallia.

## <a name="additional-resources"></a>Lisäresurssit

[Aloituspakkauksen yleiskatsaus](starter-kit-overview.md)

[Konttimoduuli](add-container-module.md)

[Ostoruutumoduuli](add-buy-box.md)

[Ostoskorimoduuli](add-cart-module.md)

[Tilauksen vahvistusmoduuli](order-confirmation-module.md)

[Ylätunnistemoduuli](author-header-module.md)

[Alatunnistemoduuli](author-footer-module.md)
