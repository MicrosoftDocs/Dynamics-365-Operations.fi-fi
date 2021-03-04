---
title: Sähköisen raportoinnin siirron siivous
description: Tässä ohjeaiheessa kerrotaan, miten ER-siirron tyhjennystoiminnon avulla voidaan ratkaista ER:n malleihin liittyviä ongelmia.
author: NickSelin
manager: AnnBe
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, ERParameters, ERMigrationCleanup
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: edb60f247b2bd6cc4ecd514e3e85bafbb681788d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686365"
---
# <a name="er-migration-cleanup"></a>Sähköisen raportoinnin siirron siivous 

[!include[banner](../includes/banner.md)]

Finance-esiintymiä hallittaessa nykyinen esiintymäsi voidaan päättää siirtää toiseen sijaintiin. Voit esimerkiksi siirtää tuotantoesiintymän uuteen eristysympäristöön. Jos määrität sähköisen raportoinnin (ER) kehyksen tallentamaan mallit Microsoft Azuren Blob-objektisäilöön, uuden eritysympäristön **DocuValue**-taulu viittaa tuotantoympäristön Blob-objektisäilöön. Tätä esiintymää ei kuitenkaan voi käyttää eristysympäristössä, koska siirtoprosessi ei tue artefaktien siirtoa Blob-objektisäilössä. Sen sijaan on odotettavissa, että uudessa sandbox-ympäristössä on Blob-tallennusympäristön esiintymä, joka ei vielä hanki ER-malleja.

Jos yrität luoda liiketoiminta-asiakirjoja suorittamalla mallia käyttävän ER-muodon, tapahtuukin poikkeus ja saat ilmoituksen puuttuvasta mallista. Sinut myös ohjataan käyttämään ER-siirron puhdistusvaihtoehtoa sekä poistamaan ja tuomaan uudelleen mallin sisältävä ER-muodon määritys.

[![ER-muodon käyttö](./media/er-migration-cleanup-run.png)](./media/er-migration-cleanup-run.png)

Näyttöön tulee samanlainen virhe, jos siirryt **Konfiguraatiot**-sivulle (**Organisaation hallinta** \> **Sähköinen raportointi** \> **Konfiguraatiot**) ja konfiguraatiot-puuhun, kun yrität poistaa mallia käyttävän ER-muotokonfiguraation.

[![ER-muodon poistaminen](./media/er-migration-cleanup-delete.png)](./media/er-migration-cleanup-delete.png)

Ratkaise sellaisten ER-mallien ongelmat, joita et voi käyttää, suorittamalla seuraavat vaiheet.

1.  Siirry **Organisaation hallinta** \> **Kausittainen** \> **Siirron tyhjennys** -sivulle.
2.  Valitse ER-muotokonfiguraatio, jota ei voi suorittaa tai poistaa.
3.  Valitse **Poista**.
4.  Vahvista valitun ER-muodon konfiguraation poistaminen.
5.  [Tuo](download-electronic-reporting-configuration-lcs.md) poistetun ER-muodon konfiguraatio nykyiseen Finance-esiintymään.

## <a name="applicability"></a>Soveltuvuus

> [Tärkeää] **Siirron uudelleenjärjestäminen** -asetus kohdistuu vain sellaisiin ER-muotokonfiguraatioihin, jotka sisältävät ei-käytettävissä olevia ER-malleja. Kun poistat ER-muodon konfiguraation **Siirron uudelleenjärjestäminen** -vaihtoehdon avulla, ER poistaa vain sovellustietokannan konfigurointiartefakteja koskevat mallit. Blob-tallennustilan asianmukaisten fyysisten tiedostojen olemassaoloa ei vahvisteta. Sen sijaan oletetaan, että niitä ei ole. Älä siis käytä **Siirron uudelleenjärjestäminen** -vaihtoehtoa **Konfiguraatiot**-sivun ER-konfiguraation poistoasetuksen vaihtoehtona. Käytä **Siirron uudelleenjärjestäminen** -vaihtoehtoa **Konfiguraatiot**-sivun ER-konfiguraation poistoasetus epäonnistuu.
>
> Kun käytät **Siirron uudelleenjärjestäminen** -vaihtoehtoa ER-muodon konfiguraation poistamiseen, kun viitattu malli on Blob-tallennustilassa, poistat vain sovellustietokannan konfigurointiartefakteja koskevat mallit. BLOB-tallennustilan mallin fyysinen tiedosto säilyy. BLOB-tallennustilan korvaaminen ei ole enää sallittua. Lisätietoja on kohdassa [KB4557217](https://fix.lcs.dynamics.com/Issue/Details?kb=4557217). Tämän lisäksi et voi enää tuoda poistettuja konfiguraatioita uudelleen käyttämällä siirron siivousta tässä ympäristössä. Tämän ongelman ratkaiseminen edellyttää, että löydät vastaavan tiedoston Blob-tallennuksessa ja poistat sen manuaalisesti.

[![ER-muodon tuominen](./media/er-migration-cleanup-import.png)](./media/er-migration-cleanup-import.png)

Samankaltainen ongelma voi ilmetä, jos siirrät sovellusinstanssin toiseen sijaintiin, jota on käytetty siirtokohteena useammin kuin kerran ja jossa Blob-säilö sisältää jo ER-mallitiedostoja.

Koska ER-muodon määrityksiä voi olla useita, tämä prosessi voi kestää kauan. Tämän vuoksi on suositeltavaa käyttää [ER-mallien varmuuskopiointi](er-backup-storage-templates.md) -tilaa ja palauttaa automaattisesti mallit, joissa on rikkinäisiä viittauksia.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]