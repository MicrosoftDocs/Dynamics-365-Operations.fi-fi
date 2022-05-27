---
title: Korjausten hallinta
description: Voit ryhmittää ongelmat systemaattisesti. Se auttaa aiemmin onnistuneiden ratkaisujen ehdottamisessa.
author: sorenva
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f969224f48cdb1f12b48b9f5d839d7c88168e87d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674250"
---
# <a name="repair-management"></a>Korjausten hallinta       

[!include [banner](../includes/banner.md)]


Korjausten hallinnassa voit ryhmittää ongelmat systemaattisesti. Se auttaa aiemmin onnistuneiden ratkaisujen ehdottamisessa.

Voit määrittää oireiden, vianmäärityksen ja ratkaisun asetukset. Kaikkia näitä voidaan käyttää myöhemmin vastaanotettaessa samanlaisia korjattavia nimikkeitä. Voit myös määrittää korjauksen vaiheet, joiden avulla korjausta voi seurata.

## <a name="setting-up-repair-management"></a>Korjausten hallinnan määrittäminen

Käytä seuraavia määrityslomakkeita syöttääksesi tiedot, joita käytetään korjauksen oireiden, vianmäärityksen ja ratkaisun määritykseen.

- **Palveluiden hallinta** \> **Määritys** \> **Korjaus** \> **Olosuhteet**.
- **Palveluiden hallinta** \> **Määritys** \> **Korjaus** \> **Oirealueet**.
-  **Palvelujen hallinta** \> **Määritys** \> **Korjaus** \> **Vianmääritysalueet**.
- **Palvelujen hallinta** \> **Määritys** \> **Korjaus** \> **Ratkaisut**.
- **Palvelujen hallinta** \> **Määritys** \> **Korjaus** \> **Korjauksen vaiheet**.

## <a name="symptoms-and-conditions"></a>Oireet ja olosuhteet

Oireet ovat asiakkaan kuvaus siitä, miten ongelma ilmenee. Oireet sisältävät asiakkaan havainnot korjaustarpeesta.

Voit määrittää oirealueita, oirekoodeja ja olosuhteita. Oirealue kattaa toimintahäiriön alueen ja oirekoodi kattaa toimintahäiriön oireen. Olosuhde kuvaa tilannetta tai ympäristöä, jossa ongelma ilmenee.

**Esimerkki**

Tietokone tuodaan korjattavaksi, koska kiintolevy vikaantuu pitkän käyttöjakson jälkeen. Kiintolevyn vika aiheuttaa sinisen virhenäytön. Tietokoneen vastaanottava huoltoteknikko syöttää seuraavat oireet ja olosuhteet:

1.  Oirealue on kiintolevy

2.  Oirekoodi on sininen virhenäyttö

3.  Olosuhde on, että kiintolevy on vikaantunut pitkän käyttöjakson jälkeen

## <a name="diagnosis-and-resolutions"></a>Vianmääritys ja ratkaisut

Vianmääritys- ja ratkaisukentät ovat tiedotteita korjauksen näkökulmasta. Nämä ovat vaiheita, jotka tekninen asiantuntija suoritti tutkiessaan ongelmaa.

Vianmääritysalue sisältää ongelman ratkaisuksi suoritettavan toiminnon. Vianmäärityskoodi kertoo, miten ongelma hoidettiin, ja ratkaisu voi olla se, että nimike korjattiin, korvattiin tai asiakas peruutti tilauksen. Jos esimerkiksi tietokone korjataan, vianmääritysalue voi olla "viallinen osa", vianmäärityskoodi "asennettiin uusi näytönohjain" ja ratkaisu "korvattu".

## <a name="repair-stages"></a>Korjauksen vaiheet

Korjauksen vaiheet osoittavat korjausprosessin etenemisen. Korjauksen vaiheella on **Valmis**-valmistumisparametri, joka osoittaa korjausrivin valmistumisen ja lopetuspäivämäärän ja ajan tallennuksen.

## <a name="applying-repair-management"></a>Korjausten hallinnan kohdistaminen

Nimikkeelle on määritettävä huoltotilauksessa huoltokohdesuhde, jotta korjauksen hallinnan voi kohdistaa nimikkeeseen. Huoltotilauksesta voi tämän jälkeen luoda korjausrivin, joka sisältää nykyisen ongelman tiedot. Korjausrivillä määritetään korjattavana oleva huoltokohde ja oireiden, vianmäärityksen ja suorituksen tiedot. Korjausriville voi luoda myös huomautuksen.

Voit luoda korjausrivejä jokaisessa korjausprosessin vaiheessa.

## <a name="create-a-repair-line-on-a-service-order"></a>Korjausrivin luominen huoltotilaukseen

1.  Avaa **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.

2.  Valitse huoltotilaus, jossa korjausta kaipaava huoltokohde on.

3.  Valitse **Korjaus** \> **Korjausrivit** avataksesi **Korjausrivit**-lomakkeen.

4.  Luo uusi rivi valitsemalla **Uusi**.

5.  Valitse huoltokohde. Voit valita minkä tahansa huoltokohteen, jolle on määritetty kohteen suhde huoltotilauksessa.

6.  Valitse mitkä tahansa korjausriville haluamasi esiintyvien oireiden, vianmäärityksen ja suorituksen arvot. Luo tarvittaessa huomautus korjausriville valitsemalla **Huomautus**-välilehti.

7.  Tallenna uusi korjausrivi valitsemalla **Tallenna**. **Luonnin päivämäärä ja aika** -kenttä **Yleinen**-välilehdellä **Korjausrivit**-lomakkeessa päivitetään tallennusajalla.

## <a name="tracking-progress-and-resolving-a-repair-issue"></a>Edistymisen seuranta ja korjausongelman ratkaisu

Voit määrittää korjausriville korjauksen vaiheet, joiden avulla korjauksen edistymistä voi jäljittää.

Kun korjausongelma on ratkaistu, voit sulkea korjausrivin. Määritä korjauksen vaiheeksi vaihe, jossa on käytössä **Valmis**-ominaisuus. Nykyinen päivämäärä ja aika rekisteröidään rivin lopetusajaksi.

## <a name="close-a-repair-line-for-a-resolved-issue"></a>Ratkaistun tapauksen korjausrivin sulkeminen

1.  Avaa **Korjausrivit**-lomake. Luo korjausrivi avaamalla seuraamalla aiemmin tässä aiheessa kerrottua menettelytapaa.

2.  Valitse se korjausrivi, jossa suljettava korjaustapaus sijaitsee.

3.  Valitse **Korjauksen vaihe** -kentässä vaihe, jossa **Valmis**-ominaisuus on käytössä.

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]