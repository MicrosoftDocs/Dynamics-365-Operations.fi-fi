---
title: Tuote on pidossa tapahtumia varten
description: Kun olet vahvistanut suunnittelutilaukset, saat virhesanoman, jossa todetaan, että nimike on tapahtumien osalta pidossa.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6654e6437a088218db116b955631be4c7e62de5f
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301276"
---
# <a name="product-is-on-hold-for-transactions"></a>Tuote on pidossa tapahtumia varten

Virhekoodi: SYS13295

## <a name="symptoms"></a>Oireet

Kun yrität vahvistaa suunnitellut tilaukset, näyttöön tulee seuraava virhesanoma:

> Tapahtumat on estetty nimikkeen %1 osalta kohteessa %2.

## <a name="cause"></a>Syy

Kun järjestelmä kuvailee estettyjä nimikkeitä, se käyttää *estetyn*, *pysäytetyn* ja *estossa olevien* ehtojen vaihtoa. Tämä virhe tarkoittaa, että nimike on määritetty tilauksen oletusasetuksissa **Pysäytetty**-tilaksi.

Jos nimike on estetty ja lisäät sen ostotilaukseen tai myyntitilausriviin, näyttöön tulee varoitussanoma. Kun nimike on estetty, osto- tai myyntitilausriviin liittyviä varastotapahtumia ei voi muokata (esimerkiksi pakkausluetteloa tai laskua kirjattaessa). Voit estää ostetun nimikkeen ja samanaikaisesti myydä nimikkeen. Tässä tapauksessa **Pysäytetty**-kenttä on valittu ostotilauksessa, mutta sitä ei ole estetty varastossa tai myyntitilauksessa.

Jotkin ehdoista voivat estää nimiketunnuksen myynnissä:

- Nimike on vielä kehitys- tai valmistusvaiheessa. Et siis halua, että sitä myydään tai varataan.
- Olet vastaanottanut useita viallisia nimikkeitä, ja viat on korjattava, ennen kuin nimikettä voi myydä.

Tämän tyyppisissä tapauksissa nimikkeen myynti voidaan estää ongelman ratkaisuun asti.

JOs nimike on estetty ja luot palautustilausrivin, saat sanoman. Et voi estää nimikesarjaa tai -erää. Jos nimikkeen osia tulee estää, tämä voidaan tehdä varastosiirroilla tai estämällä koko nimikevarasto tarvittavaksi ajaksi.

## <a name="resolution"></a>Ratkaisu

- Avaa nimikkeen **oletustilausasetukset** -sivu ja tyhjennä **Pysäytetty**-valintaruutu.
