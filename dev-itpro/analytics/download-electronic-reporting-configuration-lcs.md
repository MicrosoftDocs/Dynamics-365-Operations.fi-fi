---
title: "Lataa sähköiset raportoinnin määritykset Lifecycle Services -palvelusta"
description: "Tässä ohjeaiheessa kerrotaan, kuinka voit ladata sähköisen raportoinnin määritysten (ER)-Microsoft Dynamics Lifecycle Services (LCS)."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 9dca5dec846670da25926826f59d7bce0fa0dcea
ms.lasthandoff: 03/31/2017


---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Lataa sähköiset raportoinnin määritykset Lifecycle Services -palvelusta

Tässä ohjeaiheessa kerrotaan, kuinka voit ladata sähköisen raportoinnin määritysten (ER)-Microsoft Dynamics Lifecycle Services (LCS).

Tässä oppaassa kuvataan uusimpien sähköisten raportoinnin (ER) konfiguraatioiden lataaminen Microsoft Dynamics Lifecycle Services -palvelusta (LCS).

1.  Kirjaudu Dynamics 365 for Operations -järjestelmään yhdellä seuraavista rooleista:
    -   Sähköisen raportoinnin kehittäjä
    -   Sähköisen raportoinnin toiminnallinen konsultti
    -   Järjestelmänvalvoja

2.  Siirry **organisaation hallinta**&gt;**sähköinen raportointi**.
3.  Valitse **Konfiguraation lähteet** -osassa **Microsoft**-ruutu.
4.  Napsauta **Microsoft**-ruudussa **Säilöt**-linkkiä. [![Update-ER-from-LCS-for-MS-Open-MS-repositories-List](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)
5.  Valitse **Konfiguraatiosäilöt**-sivun ruudukossa oleva säilö, jonka tyyppi on **LCS**. Jos säilöä ei ole ruudukossa, noudata seuraavia ohjeita:
    1.  Lisää uusi säilö napsauttamalla **Lisää**-linkkiä.
    2.  Valitse säilön tyypiksi **LCS**.
    3.  Valitse **Luo säilö**.
    4.  Kirjoita säilön nimi ja kuvaus.
    5.  Valitse **OK**, niin vahvistat uuden säilön luonnin.
    6.  Valitse ruudukossa uusi **LCS**-tyypin säilö.

6.  Valitsemalla **Avaa** voit tarkastella valitun säilön ER-konfiguraatioita. [![Update-ER-from-LCS-for-MS-Make-LCS-Repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)
7.  Valitse vasemman ruudun konfiguraatioiden puurakenteessa tarvitsemasi ER-konfiguraatio.
8.  Valitse **Versiot**-pikavälilehdellä valitun ER-konfiguraation tarvittava versio.
9.  Valitse **Tuo** ladataksesi valitun version LCS-palvelusta nykyiseen Dynamics 365 for Operations -esiintymään. **Huomautus:** **Tuo**-painike ei ole käytettävissä ER-konfiguraatioversioille, jotka on jo ladattu nykyiseen Dynamics 365 for Operations -esiintymään. [![Update-ER-from-LCS-for-MS-Download-Configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

**Huomautus:** konfiguraatiot tarkistetaan tuonnin jälkeen ER-asetuksista riippuen. Voit saada ilmoituksia havaituista epäyhtenäisyysongelmista. Kyseiset ongelmat on ratkaistava, ennen kuin voit käyttää tuotua konfiguraatioversiota. Saat lisätietoja, luettelon aiheeseen liittyviä artikkeleita tämän aiheen.

<a name="see-also"></a>Lisätietoja
--------

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)


