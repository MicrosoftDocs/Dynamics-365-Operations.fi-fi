---
title: Ajoita ylläpitosuunnitelmat
description: Tässä ohjeaiheessa kerrotaan ylläpitosuunnitelmien ajoittamisesta resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b9efd5bccdccf6ea19b105f3518bb2ef35ec857e
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571274"
---
# <a name="schedule-maintenance-plans"></a>Ajoita ylläpitosuunnitelmat

[!include [banner](../../includes/banner.md)]

 

Ennaltaehkäisevän kunnossapidon ajoituksessa luodaan käyttöomaisuuksien kalenterimerkinnät käyttöomaisuudelle määritettyjen ylläpitosuunnitelmien perusteella. Voit ajoittaa kalenterimerkintöjä valittujen ylläpitosuunnitelmien, käyttöomaisuustyyppien ja resurssien mukaan.

1. Valitse **Resurssien hallinta** > **Kausittainen** > **Ennalta ehkäisevä ylläpito** > **Ajoita ylläpitosuunnitelmat**.

2. Voit valita aikavälin **Jakso**- ja **Jakson frekvenssi** -kentistä.

>[!NOTE]
>**Jakso**- ja **Jakson frekvenssi** -kentät ilmaisevat, kuinka kauas eteenpäin haluat, että huoltoaikataulu rivit luodaan luomiesi ylläpitosuunnitelmien (aikapohjainen tai laskuripohjainen) perusteella. Alla olevassa kuvassa ylläpitoaikataulurivit (= työtilausehdotukset) luodaan nykyisestä päivästä kolme kuukautta eteenpäin.

3. Valitse "kyllä" **Luo automaattisesti, jos on määritetty rivillä** -vaihtopainikkeessa, jos työtilaukset luodaan automaattisesti huoltosuunnitelmarivin mukaan.

>[!NOTE]
>Jos tämän vaihtopainikkeen arvoksi on määritetty "kyllä" *ja* **Luo automaattisesti** -valintaruutu on valittuna **Ylläpitosuunnitelmat** -kohdan ylläpitoriveillä, työtilaukset luodaan huoltosuunnitelmarivien perusteella ja myös ylläpitosuunnitelmarivit, joiden tila on "Työtilaus luotu", luodaan. Jos valittuna on vain yksi vaihtoehto (**Luo automaattisesti, jos määritetty rivillä** -vaihtopainike tai **Luo automaattisesti** -valintaruutu **Ylläpitosuunnitelmat** -lomakkeessa), vain huoltoaikataulurivit luodaan tilassa "Luotu". Tässä tapauksessa työtilauksia ei luoda.

4. On mahdollista luoda kalenterimerkintöjä, jotka perustuvat ylläpitosuunnitelmiin (aika tai laskuri), käyttöomaisuuseriin, resurssityyppeihin, toiminnallisiin sijainteihin ja toiminnallisiin sijaintityyppeihin. Napsauta **Suodata**-painiketta ja tee valintasi tarvittaessa.

- Toiminnallisten sijaintien ylläpitosuunnitelmien ajoittamiseen liittyen: Jos päivität resurssin tyyppien, valmistajien ja mallien asetukset ylläpitosuunnitelmille **Kaikki toiminnalliset sijainnit** >  **Ylläpitosuunnitelmat** -pikavälilehdessä ja olet suunnitellut kunnossapitosuunnitelmat, aiemmin luodut kyseiseen toiminnalliseen sijaintiin liittyvät kunnossapitoaikataulun merkinnät poistetaan automaattisesti. Jotta voit luoda uusia kalenterimerkintöjä, jotka vastaavat toiminnallisen sijainnin päivitettyjä ylläpitosuunnitelman asetuksia, sinun on suoritettava kyseiselle toiminnalliselle sijainnille uusi ylläpitosuunnitelman aikataulu. Lisätietoja käyttöomaisuuden tyyppien, valmistajien ja mallien määrittämisestä toiminnallisissa sijainneissa on kohdassa [Luo toiminnalliset sijainnit](../functional-locations/create-functional-locations.md).

>*Esimerkki:* Haluat luoda huoltosuunnitelman tiettyä toiminnallista sijaintia varten, jolloin kaikki kyseiseen toimintapaikkaan määritetyt käyttökohteet sisällytetään valittuna aikana, kun ajoitat huoltosuunnitelmaa. Tässä tapauksessa luot huoltosuunnitelman ja valitset tietyn toimintosijainnin, mutta ET lisää huoltosuunnitelmaan mitään resursseja. Tuloksena on, että kun ajoitat kyseisen ylläpitosuunnitelman, kunnossapitoaikataulurivit luodaan kaikille kyseiseen toimintapaikkaan liittyville resursseille.

- Jos teet muutoksia käyttöomaisuuden tyyppeihin, valmistajiin tai malleihin kohdassa **Resurssityypit**, muutokset vaikuttavat vain uusiin käyttöomaisuuseriin, jotka käyttävät päivitettyä käyttöomaisuuslajia. Lue lisää käyttöomaisuustyyppien määrityksestä kohdassa [Resurssityypit](../setup-for-objects/object-types.md).  

5. Aloita käyttöomaisuuksien ylläpitoaikataulumerkintöjen luominen valitsemalla **OK**. Luodut merkinnät näkyvät **Kaikki ylläpitoaikataulut** -luettelosivulla. Seuraavassa kuvassa on esimerkki **Ajoita ylläpitosuunnitelmat** -valintaikkunasta.

![Kuva 1](media/09-preventive-maintenance.png)

- **Ajoita ylläpitosuunnitelmat** -valintaikkunassa voit määrittää erätyöt **Suorita taustalla** -pikavälilehdessä, jolloin kalenterimerkinnät luodaan automaattisesti säännöllisin väliajoin.  
- Kun ajoitat ennaltaehkäisevän huollon, ylläpitoaikataulurivejä, joiden alkamispäivämäärä ja -aika ovat aikaisempia kuin järjestelmän päivämäärä ja kellonaika, ei luoda.  

Alla olevassa kuvassa on graafinen esimerkki aikapohjaisesta ylläpitosuunnitelman laskennasta.  

![Kuva 2](media/10-preventive-maintenance.jpg)

Laskuripohjaisiin ylläpitosuunnitelmiin liittyen: Alla olevissa kuvissa näytetään kaksi eri laskurin rekisteröinnin jaksoa. Ne perustuvat ylläpitosuunnitelmaan, joka on määritetty käyttöomaisuuserälle "V0001", ja odottaa, että käyttöomaisuuserää (autoa) ajetaan noin 2 000 km joka kuukausi.

Ensimmäisessä esimerkissä odotettua 2 000 km:ä ei saavuteta kuukausittain. Laskuripohjaisen ylläpitosuunnitelman mukaan kynnysarvo on 2 000 km, eli kun huoltosuunnitelman ajoitus suoritetaan, huoltoaikataulurivi luodaan aina, kun 2 000 kilometrin raja saavutetaan. Esimerkissä 1 on neljä rekisteröitymisriviä, mutta 2 000 kilometrin raja saavutetaan vain kerran. Tämä tarkoittaa sitä, että kun suoritat ylläpitosuunnitelmat tälle käyttöomaisuuserälle (esimerkiksi kolmen kuukauden jaksona) luodaan vain yksi huoltoaikataulurivi.

Seuraavassa kuvassa 2 000 km tai enemmän kirjataan kuukausittain. Tämän vuoksi luodaan kolme kunnossapitoriviä, jos tämän käyttöomaisuuserän huoltosuunnitelmat ajoitetaan kolmen kuukauden ajaksi. 

Tässä kuvatut esimerkit osoittavat, että kaikki käyttöomaisuuserään tehdyt laskurikirjaukset näyttävät trendin, joka kuvaa käyttöomaisuuserän kulumista. Tätä trendiä käytetään laskuperusteena ylläpitosuunnitelman ajoituksen aikana.

![Kuva 3](media/11-preventive-maintenance.png)

![Kuva 4](media/12-preventive-maintenance.png)

