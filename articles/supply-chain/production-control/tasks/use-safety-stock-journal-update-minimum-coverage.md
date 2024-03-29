---
title: Varmuusvaraston kirjauskansion käyttäminen minimikattavuuden päivittämiseen
description: Seuraavassa menettelyssä kuvataan, miten voit laskea vähimmäiskattavuuden ehdotukset historiatapahtumiin perustuen ja päivittää nimikekattavuuden ehdotusten mukaiseksi.
author: johanhoffmann
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ae2209fc2412a4a67b46d6eb82ecb70aafc0159
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573606"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a>Varmuusvaraston kirjauskansion käyttäminen minimikattavuuden päivittämiseen

[!include [banner](../../includes/banner.md)]

Seuraavassa menettelyssä kuvataan, miten voit laskea vähimmäiskattavuuden ehdotukset historiatapahtumiin perustuen ja päivittää nimikekattavuuden ehdotusten mukaiseksi. Tämä tehdään varmuusvaraston kirjauskansion avulla. Tämän tehtävän luomisessa käytetty esittely-yritys on USMF. Tämä tehtävä on tarkoitettu tuotannon suunnittelijalle minimikattavuuden ylläpitoa varten.


## <a name="create-a-new-safety-stock-journal-name"></a>Uuden varmuusvaraston kirjauskansion nimen luominen
1. Siirry kohtaan **Siirtymisruutu** > **Pääsuunnitelu > Asetukset > Varmuusvarastokirjauskansion nimet**.
2. Valitse **Uusi**.
3. Kirjoita "Materiaali" **Nimi**-kenttään.
4. Kirjoita **Kuvaus**-kentän arvoksi Materiaali.
5. Sulje sivu.

## <a name="create-a-safety-stock-journal"></a>Luo varmuusvaraston kirjauskansio
1. Siirry **siirtymisruudussa** kohtaan **Pääsuunnittelu > Pääsunnittelu > Suorita > Varmuusvaraston laskenta**.
2. Valitse **Uusi**.
3. Anna tai valitse arvo **Nimi**-kentässä. Valitse luomasi varmuusvaraston kirjauskansion nimi, esimerkiksi Materiaali.  
4. Valitse **Luo rivit**.
5. Syötä päivämäärä **Päivämäärästä**-kenttään.  
6. Kirjoita päivämäärä **Päivämäärään**-kenttään.
7. Valitse **OK**. Tämä luo rivit dimensioille, joilla on varastotapahtumia.  

## <a name="calculate-proposal"></a>Laske ehdotus
1. Napsauta kohtaa **Laske ehdotus**.
2. Valitse **Käytä keskimääräistä varasto-ottoa läpimenoaikana** -vaihtoehto.
3. Aseta **kerroinarvoksi** 10. Kerroinarvoa käytetään ehdotuksen oikaisemiseen. Koska esittelytiedoissa on vain muutamia tapahtumia, kerroin on määritettävä, jos haluat realistisen ehdotuksen.  
4. Valitse **OK**. Etsi M0002 ja M0003 alaspäin selaamalla. Näytä **Laskettu vähimmäismäärä** -sarake.   

## <a name="update-minimum-quantity"></a>Päivitä vähimmäismäärä
1. Syötä numero **Uusi vähimmäismäärä** -kenttään. Päivitä uusi vähimmäismäärä vastaavaan lasketun vähimmäismäärän arvoa. Jos laskettu vähimmäismäärä on nolla, voit syöttää haluamasi tulevan arvon. Voit esimerkiksi syöttää lasketun vähimmäismäärän tähän kenttään M0002 sisältävälle varastolle 12.  
2. Etsi haluamasi tietue luettelosta ja valitse se. Voit valita esimerkiksi M0002 sisältävän varaston 12.  
3. Syötä numero **Uusi vähimmäismäärä** -kenttään. Päivitä uusi vähimmäismäärä vastaavaan lasketun vähimmäismäärän arvoa. Jos laskettu vähimmäismäärä on nolla, voit syöttää haluamasi tulevan arvon.  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>Kirjaa uusi vähimmäismäärä ja vahvista tulos
1. Valitse **Kirjaa**.
2. Valitse **OK**.
3. Käytä **Nimiketunnus**-kentän linkkiä napsauttamalla.
4. Käytä **Nimiketunnus**-kentän linkkiä napsauttamalla.
5. Valitse **toimintoruudussa** Suunnitelma.
6. Valitse **Nimikekattavuus**. Huomaa, että **vähimmäismääräksi** on päivitetty uusi vähimmäismäärä varmuusvaraston kirjauskansiosta.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]