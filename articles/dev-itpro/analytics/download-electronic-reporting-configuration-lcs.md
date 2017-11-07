---
title: "Lataa sähköiset raportoinnin määritykset Lifecycle Services -palvelusta"
description: "Tässä aiheessa neuvotaan, miten Microsoft Dynamics 365 for Operations -järjestelmän sähköisen raportoinnin (ER) konfiguraatiot ladataan Microsoft Dynamics Lifecycle Services -palvelusta (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a4411b25285128c849a715fdc7a2f5fe51580a3b
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Lataa sähköiset raportoinnin määritykset Lifecycle Services -palvelusta

[!include[banner](../includes/banner.md)]


Tässä aiheessa neuvotaan, miten Microsoft Dynamics 365 for Operations -järjestelmän sähköisen raportoinnin (ER) konfiguraatiot ladataan Microsoft Dynamics Lifecycle Services -palvelusta (LCS).

Tässä oppaassa kuvataan uusimpien sähköisten raportoinnin (ER) konfiguraatioiden lataaminen Microsoft Dynamics Lifecycle Services -palvelusta (LCS).

1.  Kirjaudu Finance and Operationsiin yhdellä seuraavista rooleista:
    -   Sähköisen raportoinnin kehittäjä
    -   Sähköisen raportoinnin toiminnallinen konsultti
    -   Järjestelmänvalvoja

2.  Siirry kohtaan **Organisaation hallinto** &gt; **Sähköinen raportointi**.
3.  Valitse **Konfiguraation lähteet** -osassa **Microsoft**-ruutu.
4.  Napsauta **Microsoft**-ruudussa **Säilöt**-linkkiä. [![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)
5.  Valitse **Konfiguraatiosäilöt**-sivun ruudukossa oleva säilö, jonka tyyppi on **LCS**. Jos säilöä ei ole ruudukossa, noudata seuraavia ohjeita:
    1.  Lisää uusi säilö napsauttamalla **Lisää**-linkkiä.
    2.  Valitse säilön tyypiksi **LCS**.
    3.  Valitse **Luo säilö**.
    4. Noudata luvananto-ohjeita tarvittaessa.
    5.  Kirjoita säilön nimi ja kuvaus.
    6.  Valitse **OK**, niin vahvistat uuden säilön luonnin.
    7.  Valitse ruudukossa uusi **LCS**-tyypin säilö.

6.  Valitsemalla **Avaa** voit tarkastella valitun säilön ER-konfiguraatioita. [![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)
7.  Valitse vasemman ruudun konfiguraatioiden puurakenteessa tarvitsemasi ER-konfiguraatio.
8.  Valitse **Versiot**-pikavälilehdellä valitun ER-konfiguraation tarvittava versio.
9.  Lataa valittu versio LCS-palvelusta nykyiseen Finance and Operations -esiintymään valitsemalla **Tuo**. **Huomautus:** **Tuo**-painike ei ole käytettävissä ER-konfiguraatioversioille, jotka on jo ladattu nykyiseen Finance and Operations -esiintymään. [![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

**Huomautus:** konfiguraatiot tarkistetaan tuonnin jälkeen ER-asetuksista riippuen. Voit saada ilmoituksia havaituista epäyhtenäisyysongelmista. Kyseiset ongelmat on ratkaistava, ennen kuin voit käyttää tuotua konfiguraatioversiota. Lisätietoja saat tähän aiheeseen liittyvistä artikkeleista.

<a name="see-also"></a>Lisätietoja
--------

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)




