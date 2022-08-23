---
title: Kuvien ja muotojen upottaminen luomiisi asiakirjoihin ER:n avulla
description: Tässä artikkelissa kuvataan, kuinka sähköisen raportointityökalulla voidaan luoda yritysasiakirjoja, joissa on upotettuja kuvia ja muotoja.
author: kfend
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.custom: 27621
ms.assetid: ''
ms.search.form: EROperationDesigner, ERParameters
ms.openlocfilehash: 0bb652f245db93424aeadcaadf2ad393945e616b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280985"
---
# <a name="embed-images-and-shapes-in-documents-that-you-generate-by-using-er"></a>Kuvien ja muotojen upottaminen luomiisi asiakirjoihin ER:n avulla

[!include [banner](../includes/banner.md)]

Voit käyttää sähköisen raportoinnin (ER) työkalua suunnitellaksesi raportteja, joita voit suorittaa tarvittavien sähköisten tiedostojen luomiseksi. Voit käyttää Microsoft Excel- tai Microsoft Word -asiakirjoja raportin asettelun määrittämiseen. ER-toimintojen suunnitteluohjelmalla voit liittää Excel- tai Word-asiakirjan raportin malliksi. Liitetyn mallin nimetyt elementit on liitetty ER-raportin muotoelementteihin. Raportin muotoelementit ovat sidoksissa tietolähteisiin. Nämä elementit määrittävät tiedot, jotka lisätään luotuihin asiakirjoihin suorituksen aikana.

Tämä uusi ominaisuus laajentaa Microsoft Office -muotoisten asiakirjojen luomisen ER-toimintoja. Lisätietoja on seuraavissa tehtäväoppaissa. Löydät nämä tehtäväoppaat 7.5.4.3 Acquire/Develop IT service/solution components (10677) -liiketoimintaprosessista.

- ER Suunnittele kokoonpano, jolla raportit voi luoda OPENXML-muodossa
- ER Suunnittele kokoonpano, jolla raportit voi luoda Microsoft WORD -muodossa

## <a name="embed-an-image-in-an-excel-document"></a>Kuvan upottaminen Excel-asiakirjaan

### <a name="embed-an-image-in-an-excel-worksheet"></a>Kuvan upottaminen Excel-laskentataulukkoon

Ensin sinun on lisättävä kuvalle paikkamerkki Excel-asiakirjaan. Avaa Excel-laskentataulukko ja lisää kuva paikkamerkkinä kuvalle, jonka lisäät myöhemmin. Käytä sitten ER-työkalua lisätäksesi uuden ER-muotokonfiguraation, joka sisältää suunnittelemasi raportin. Liitä Excel-laskentataulukko mallina raportin muodolle ja tuo sitten laskentataulukon sisältö ER-muodossa. Muodon määritys luodaan automaattisesti. Lisäämäsi kuvan paikkamerkki sisällytetään ER-muotokonfiguraatioon **SOLU**-elementtinä.

> [!NOTE]
> Voit määrittää muodon määrityksen manuaalisesti tuomisen sijaan. Kun tallennat muutokset, muoto vahvistetaan.

Sido sitten ER-muodon **SOLU**-elementti kenttään muodon tietolähteestä, joka antaa kuvan tiedot binaarimuodossa suorituksen aikana. Kun muodon tietolähteenä käytetään ER-tietomallia, kentän tietotyypin on oltava [Säilö](er-formula-supported-data-types-composite.md#container). Tällä hetkellä ER-tietomallin kenttä, jonka tietotyyppi on [Säilö](er-formula-supported-data-types-composite.md#container), voidaan sitoa moniin erityyppisiin tietolähteisiin, jotka palauttavat kuvia binäärimuodossa. Voit käyttää tietotaulukossa olevaa kenttää ja tietotaulukon tietueeseen liitettyä tiedostoa tiedostojen hallintakehyksen avulla.

> [!IMPORTANT]
> - Jos haluat täyttää Excel-mallilla luomassasi asiakirjassa olevan kuvan paikkamerkin, ER-muodon täytyy sisältää **SOLU**-elementti, joka viittaa Excel-mallissa olevaan nimettyyn kuvaelementtiin. Muussa tapauksessa raportin tuloksessa ei näytetä kuvan paikkamerkkiä. Jos **SOLU**-elementin sidos ei palauta mitään tietoja suorituksen aikana, luotu asiakirja näyttää mallista saadun kuvan paikkamerkin. Jos haluat piilottaa kuvan luomastasi asiakirjasta, määritä **SOLU**-elementti ja määritä, että **Käyttöönotto**-lausekkeen tulisi palauttaa **EPÄTOSI**-arvo.
> - Käytä Excel-mallissa yksilöivää nimeä jokaiselle elementille. Näitä elementtejä ovat kuvat ja solut. Jos annat usealla elementille saman nimen, luodun raportin sisältö on epäselvä ja hämmentävä.

### <a name="embed-images-in-the-header-and-footer-of-an-excel-worksheet"></a>Kuvien upottaminen Excel-laskentataulukon ylä- ja alatunnisteeseen

Käytä Excel-työkirjaa mallina määrittääksesi raportin asettelun. Työkirja voi sisältää useita laskentataulukoita, joista jokainen voidaan suunnitella siten, että siinä on ylä- ja alatunniste. Excel tukee enintään kolmea kuvaa kunkin laskentataulukon ylä- ja alatunnisteessa. Kuvat voidaan tasata vasemmalle, oikealle tai keskelle.

Voit hallita Finance-versiossa 10.0.21 ylä- ja alatunnisteiden kuvia, jotka Excel-mallin sisältävä ER-malli on luonut.

Jos haluat näyttää luodun asiakirjan ylä- tai alatunnisteessa oletuskuvan, voit lisätä kuvan ER-mallin laskentataulukon ylä- tai alatunnisteeseen. Jos haluat käyttää tätä kuvaa ER-muodossa, sinun täytyy lisätä **Kuva**-komponentti muodon [Ylätunniste](er-fillable-excel.md#header-component)- tai [Alatunniste](er-fillable-excel.md#footer-component)-komponentin alle. Määritä **Kuva**-komponentille haluamasi tasaus. 

Voit käyttää **Kuva**-komponenttia myös asettaaksesi kuvan luodun asiakirjan ylä- tai alatunnisteeseen suorituksen aikana, vaikka malli ei sisältäsi oletuskuvaa. Jos haluat määrittää luodun tiedoston ylä- tai alatunnisteeseen lisättävän mediasisällön joko uutena kuvana tai oletuskuvan korvaavana kuvana, sinun täytyy sitoa **Kuva**-elementti [Säilö](er-formula-supported-data-types-composite.md#container)-tyyppiseen tietolähteeseen, joka edustaa kuvaa binäärimuodossa.

Jokainen **Ylätunniste**- tai **Alatunniste**-komponentti voi sisältää yhden **Kuva**-komponentin jokaiselle tuetulle tasaukselle: **Vasen**, **Keskellä** ja **Oikea**.

**Kuva**-komponentin **Skaalaa korkeus** -ominaisuus sallii sinun käyttää määritettyä sidosta kuvan koon hallitsemiseen:

- Valitse **Alkuperäinen**, jos haluat säilyttää kuvan alkuperäisen koon.
- Valitse **Suhteellinen**, jos haluat skaalata kuvan korkeuden suhteessa kuvan sisältämän ylä- tai alatunnisteen korkeuteen.

    - Tällöin kuvan korkeus on määritettävä sen sisältämän ylä- tai alatunnisteen prosenttiosuutena.
    - Jos skaalausarvo ylittää 100 prosenttia, kuva saattaa asettua päällekkäinen vastaavan laskentataulukon tietoalueen kanssa.
    - Jos kuvan korkeutta muutetaan skaalausta käytettäessä, myös sen leveyttä muutetaan kuvan alkuperäisen kuvasuhteen säilyttämiseksi.

- Valitse **Absoluuttinen**, jos haluat muuttaa kuvan kokoa suunnittelun aikana annettujen korkeus- ja leveysarvojen (pikseleinä) mukaisesti.

    - Jos määritetty korkeus ylittää ylä- tai alatunnisteen korkeuden, kuva saattaa asettua päällekkäinen vastaavan laskentataulukon tietoalueen kanssa.

Voit myös käyttää **Kuva**-komponentin **Käytössä**-komponenttia hallitaksesi tämän komponentin avulla luotuun asiakirjaan lisätyn kuvan näkyvyyttä.

> [!NOTE]
> Sinun täytyy käyttää ER-muodon suunnittelutoimintoa lisätäksesi **Kuva**-komponentin muokattavaan ER-muotoon. Et voi lisätä komponenttia, kun käytät liiketoiminta-asiakirjan mallin muokkaamiseen [Liiketoiminta-asiakirjojen hallinta](er-business-document-management.md) -työtilaa.

Katso lisätietoja tästä ominaisuudesta noudattamalla kohdassa [ER-muodon suunnittelu Excel-muotoisen raportin luomiseksi ja kuvien upottamiseksi sivun ylä- ja alatunnisteisiin](er-embed-images-header-footer-excel-reports.md) kuvattuja ohjeita.

## <a name="embed-a-shape-in-an-excel-document"></a>Muodon upottaminen Excel-asiakirjaan

Ensin sinun on lisättävä muodolle paikkamerkki Excel-asiakirjaan. Avaa Excel-työkirja ja valitse muodon paikkamerkiksi **Muoto**, **Tekstiruutu** tai **WordArt**. Käytä sitten ER-työkalua lisätäksesi uuden ER-muotokonfiguraation, joka sisältää suunnittelemasi raportin. Liitä Excel-laskentataulukko mallina raportin muodolle ja tuo sitten laskentataulukon sisältö ER-muodossa. Muodon määritys luodaan automaattisesti. Lisäämäsi muodon paikkamerkki sisällytetään ER-muotokonfiguraatioon **SOLU**-elementiksi, joka viittaa nimettyyn Excel-muotoelementtiin.

> [!NOTE]
> Voit määrittää muodon määrityksen manuaalisesti tuomisen sijaan. Kun tallennat muutokset, muoto vahvistetaan.

Sido sitten ER-muodon **SOLU**-elementti kenttään muodon tietolähteestä, joka tarjoaa tiedot suorituksen aikana. Nämä tiedot voidaan muuntaa tekstimerkkijonoksi. Kun ER-muodon **SOLU**-elementti viittaa muotoelementtiin, jonka Excel-malli tukee tekstiä, tämän sidoksen suorituksen aikana tarjoama teksti näytetään luotuun asiakirjaan sisältyvässä muodossa.

> [!IMPORTANT]
> - Jos haluat käyttää muodon paikkamerkin sisältävää Excel-mallia uuden asiakirjan luomiseen, ER-muodon täytyy sisältää Excel-muotoelementtiin viittaava **SOLU**-elementti. Muussa tapauksessa raportin tuloksessa ei näytetä muodon paikkamerkkiä. Jos nimettyyn Excel-muotoelementtiin viittaavan **SOLU**-elementin sidonta ei palauta tietoja suorituksen aikana, luodussa asiakirjassa näytetään Excel-mallista saadun muodon paikkamerkin teksti. Jos haluat piilottaa muodon luomastasi asiakirjasta, määritä nimettyyn Excel-muotoelementtiin viittaava **SOLU**-elementti ja määritä, että **Käyttöönotto**-lausekkeen tulisi palauttaa **EPÄTOSI**-arvo.
> - Käytä Excel-mallissa yksilöivää nimeä jokaiselle elementille. Näitä elementtejä ovat muodot ja solut. Jos annat usealla elementille saman nimen, luodun raportin sisältö on epäselvä ja hämmentävä.

## <a name="embed-an-image-in-a-word-document"></a>Kuvan upottaminen Word-asiakirjaan
> [!IMPORTANT]
> Voit käyttää uudelleen Excel-mallia käyttävää ER-muotoa luodaksesi asiakirjoja, jotka sisältävät upotettuja kuvia. Varmista, että ER-muodon **SOLU**-elementille on määritetty nimi, joka viittaa Excelin nimettyyn kuvaelementtiin ja joka on sidottu tietolähteeseen, joka palauttaa kuvan suorituksen aikana.

Ensin sinun täytyy määrittää Word-asiakirjan asettelu. Käytä **Kuvan sisältö** -ohjausobjektia luodaksesi paikkamerkin upotetulle kuvalle. Tämän ohjausobjektin käyttö edellyttää, että **Kehittäjä**-välilehti on näkyvissä Wordin valintanauhassa.

Poista sitten Excel-malli ER-muodosta ja liitä Word-malliasiakirja. Päivitä viittaus malliin ja tallenna muutoksesi. Tämänhetkisen ER-muodon rakenne tallennetaan Word-malliin uutena mukautettuna XML-osana, jonka nimi on **Raportti**.

Tallenna sitten Word-malli tämänhetkistä ER-muotoa varten paikalliselle tietokoneellesi. Avaa malli ja avaa **XML-määritys**-ruutu. Etsi mukautettu XML-osa, jonka nimi on **Raportti**, ja osoita sitten ER-raportissa olevaan **SOLU**-elementtiin, joka on sidottu tietolähteeseen, joka palauttaa kuvan binäärimuodossa. Yhdistä tämän XML-osan nimike valittuun **Kuvan sisältö** -ohjausobjektiin ja tallenna muutoksesi.

[![upota kuvia.](./media/embed-images-shapes-01.png)](./media/embed-images-shapes-01.png)

Poista lopuksi Word-malli ER-muodosta ja liitä Word-asiakirja, joka sisältää yhdistetyt mukautetut XML-osat. Päivitä muodon viite malliin ja tallenna tähän ER-muotoon tekemäsi muutokset.

## <a name="more-information"></a>Lisätietoja
Voit tutustua tämän ominaisuuden yksityiskohtiin tehtäväoppaiden **ER Raporttien tekeminen MS Office -muodoissa ja upotettujen kuvien kanssa** -joukon avulla. Nämä tehtäväoppaat näyttävät, miten voit upottaa yrityksen logon kuvat ja valtuutetun henkilön allekirjoituksen maksettaviin sekkeihin, jotka on luotu käyttämällä Excel- ja Word-asiakirjojen ER-työkalua.

Seuraavassa taulukossa luetellaan tiedostot, jotka tarvitaan **ER Raporttien tekeminen MS Office -muodoissa ja upotettujen kuvien kanssa** -tehtäväoppaiden suorittamiseen. Lataa ja tallenna tiedostot paikalliselle tietokoneellesi.

| kuvaus                                          | Tiedostonimi                   |
|------------------------------------------------------|-----------------------------|
| ER-tietomallin konfigurointi                          | [Model for cheques.xml](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| ER-muodon konfigurointi                              | [Cheques printing format.xml](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| Yrityksen logokuva                                   | [Yrityksen logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| Allekirjoituksen kuva                                      | [Allekirjoituksen kuva.png](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| Vaihtoehtoisen allekirjoituksen kuva                          | [Allekirjoituksen kuva 2.png](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| Microsoft Word -malli sekkien tulostukseen  | [Sekkimalli Word.docx](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |
| Microsoft Excel -malli sekkien tulostukseen | [Cheque template.xlsx](https://download.microsoft.com/download/1/f/6/1f671963-73aa-48d5-ae69-45f21fe7dfb4/Cheque%20template.xlsx)        |

Seuraavassa kuvassa on esimerkki Excel-mallista luodun maksettavan sekin koevedoksesta.

[![Maksettavan sekin koevedos.](./media/embed-images-shapes-02.png)](./media/embed-images-shapes-02.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
