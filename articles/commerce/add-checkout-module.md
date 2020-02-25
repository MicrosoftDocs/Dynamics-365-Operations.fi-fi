---
title: Kassamoduuli
description: Tässä ohjeaiheessa kuvataan, miten kassamoduuli lisätään sivulle ja miten pakolliset ominaisuudet määritetään.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: 3805c0faabc8afc3decffb924b7f25332ff1ab16
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025387"
---
# <a name="checkout-module"></a>Kassamoduuli


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kuvataan, miten kassamoduuli lisätään sivulle ja miten pakolliset ominaisuudet määritetään.

## <a name="overview"></a>Yleiskatsaus

Kassamoduuli on erityinen säilö, joka isännöi kaikkia sellaisia moduuleja, jotka tarvitaan tilauksen luomista varten. Se sisältää vaiheittaisen työnkulun, jota käyttämällä asiakas syöttää kaikki tarvittavat tiedot ostoa varten. Se taltioi toimitusosoitteen, toimitustavan ja laskutustiedot. Siinä on myös tilauksen yhteenveto ja muita asiakkaan tilaukseen liittyviä tietoja.

Kassamoduuli hahmontaa tiedot ostoskorin tunnuksen mukaan. Tämä ostoskorin tunnus tallennetaan selaimen evästeeksi. Ostoskorin tunnus on pakollinen, jotta kassamoduulin tiedot kuten tilauksen nimikkeet, kokonaissumma ja alennukset, voidaan hahmontaa.

## <a name="checkout-module-properties"></a>Kassamoduulin ominaisuudet

Kassamoduuli näyttää tilauksen yhteenvedon ja tilauksen tekemiseen tarvittavat toiminnot. Kaikkien tilauksen tekemiseen tarvittavien asiakastietojen keräämistä varten kassamoduuliin on lisättävä lisämoduuleja. Niinpä vähittäismyyjät voivat lisätä mukautettuja moduuleja kassatyönkulkuun tai jättää niitä pois omien tarpeiden mukaan.

### <a name="modules-that-can-be-used-in-the-checkout-module"></a>Moduulit, joita voidaan käyttää kassamoduulissa

- **Toimitusosoite** – Tämän moduulin avulla asiakas voi lisätä tai valita tilauksen toimitusosoitteen. Jos asiakas on kirjautunut sisään, kaikki kyseiselle asiakkaalle aiemmin tallennetut osoitteet näytetään. Asiakas voi valita näistä osoitteista. Asiakas voi myös lisätä uuden osoitteen. Toimitusosoitetta käytetään kaikissa tilauksen nimikkeissä, jotka edellyttävät toimitusta. Sitä ei voi mukauttaa yksittäisille rivinimikkeille. Toimitusosoitteen muodot määritetään kullekin maalle tai alueelle. Maa-/aluekohtaiset säännöt tulevat voimaan tässä moduulissa. Vaikka tämä moduuli ei sisällä osoitteen vahvistusta, osoitteen tarkistus voidaan toteuttaa mukautuksen avulla. Jos tilauksessa on vain myymälästä noudettavia nimikkeitä, tämä moduuli piilotetaan automaattisesti.
- **Toimitusvaihtoehdot** – Tämän moduulin avulla asiakas voi valita tilauksen toimitusvaihtoehdon. Toimitusvaihtoehdot perustuvat toimitusosoitteeseen. Jos toimitusosoitetta muutetaan, toimitusvaihtoehdot on noudettava uudelleen. Jos tilauksessa on vain myymälästä noudettavia nimikkeitä, tämä moduuli piilotetaan automaattisesti.
- **Kassa-osan säilö** – Tämä moduuli on säilö, jonka sisään asetetaan useita moduuleja. Ne luovat osan kassatyönkulun sisälle. Tähän säilöön voi asettaa esimerkiksi kaikki maksuun liittyvät moduulit, jolloin ne näkyvät yhtenä osana. Tämä moduuli vaikuttaa vain työnkulun asetteluun.
- **Lahjakortti** – Tämän moduulin avulla asiakas voi maksaa tilauksen käyttämällä lahjakorttia. Tämä tukee vain Microsoft Dynamics 365 Commercen lahjakortteja. Tilaukseen voi käyttää yhtä tai useaa lahjakorttia. Jos lahjakortin saldo ei kata ostoskorin summaa, lahjakortti voidaan yhdistää toiseen maksutapaan. Lahjakortteja voi lunastaa vain, jos asiakas on kirjautunut sisään.
- **Kanta-asiakkuuspisteet** – Tämän moduulin avulla asiakas voi maksaa tilauksen käyttämällä kanta-asiakkuuspisteitä. Se sisältää yhteenvedon käytettävissä olevista ja vanhenevista pisteistä. Sen avulla asiakas voi valita lunastettavien pisteiden määrän. Jos asiakas ei ole kirjautunut sisään tai ei ole kanta-asiakasohjelman jäsen tai jos ostoskorin kokonaissumma on 0 (nolla), tämä moduuli piilotetaan automaattisesti.
- **Maksu** – Tämän moduulin avulla asiakas voi maksaa tilauksen käyttämällä luottokorttia. Jos ostoskorin kokonaissumma katetaan kanta-asiakkuuspisteillä tai lahjakortilla tai jos summa on 0 (nolla), tämä moduuli piilotetaan automaattisesti. Luottokortin integroinnin tässä moduulissa tarjoaa Adyen-maksuyhdistin. Lisätietoja tämän yhdistimen käyttämisestä on kohdassa [Dynamics 365:n Adyen-maksuyhdistin](dev-itpro/adyen-connector.md).
- **Laskutusosoite** – Tämän moduulin avulla asiakas voi antaa laskutustiedot. Adyen käsittelee nämä tiedot yhdessä luottokorttitietojen kanssa. Tämä moduuli sisältää vaihtoehdon, jonka avulla asiakkaat voivat käyttää laskutusosoitetta toimitusosoitteena.
- **Yhteystiedot** – Tämän moduulin avulla asiakas voi lisätä tai muuttaa tilauksen yhteystietoja (sähköpostiosoitetta).
- **Tekstilohko** – Tämä moduuli sisältää kaiken viestinnän, jota sisällönhallintajärjestelmä (CMS) ohjaa. Viestintää voi olla esimerkiksi seuraava viesti: Jos tilaamisessa on ongelmia, soita numeroon 1-800-Fabrikam. 

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit -käyttö

Useimmat kassatiedot, kuten toimitusosoite ja toimitustapa, tallennetaan ostoskoriin. Niitä käsitellään tilauksen osana. Ainoa poikkeus on luottokorttitiedot. Nämä tiedot käsitellään suoraan Adyen-maksuyhdistimen avulla. Maksu on vahvistettu, mutta sitä ei ole veloitettu.

## <a name="add-a-checkout-module-to-a-new-page-and-set-the-required-properties"></a>Lisää kassamoduuli uudelle sivulle ja määritä pakolliset ominaisuudet.

Voit lisätä kassamoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Siirry kohtaan **Osa \> Uusi osa** ja anna uudelle osalle nimeksi **Kassan osa**.
1. Lisää osaan kassamoduuli.
1. Lisää kassamoduuliin otsikko.
1. Lisää toimitusosoite, toimitusvaihtoehdot, kassan osan säilö- ja yhteystietomoduulit. 
1. Lisää kassaosan säilömoduulissa lahjakortti-, kanta-asiakaspiste- ja maksumoduulit. Tällä tavoin varmistat, että kaikki maksutavat näkyvät yhdessä osassa.
1. Tallenna ja esikatsele osa. Joitakin moduuleista ei ehkä hahmonneta esikatselussa, koska niissä ei ole ostoskorikontekstia.
1. Kun osan muokkaus on valmis, julkaise se.
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
