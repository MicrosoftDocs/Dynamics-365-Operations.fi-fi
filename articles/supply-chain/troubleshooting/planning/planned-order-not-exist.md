---
title: Järjestelmä ei löydä suunniteltua tilausta useiden tilausten työvaiheiden aikana
description: "\"Suunniteltu tilaus ei ole olemassa\" -virhe ilmenee, kun teet työvaiheita useille suunnitelluille tilauksille ja vähintään kaksi tilausta kuuluu samalle nimiketunnukselle."
author: t-benebo
ms.date: 12/07/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo_ReqTransPoMarkChangeType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-12-07
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 0ece4a331b63b86e896c5b337a58185ed3ea1049
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920799"
---
# <a name="the-system-cant-find-a-planned-order-during-operations-on-multiple-orders"></a>Järjestelmä ei löydä suunniteltua tilausta useiden tilausten työvaiheiden aikana

Virhekoodi: SYS24774

## <a name="symptoms"></a>Oireet

Saat seuraavan virhesanoman, kun yrität suorittaa toimintoa useille suunnitelluille tilauksille samanaikaisesti, ja vähintään kaksi tilausta kuuluu samaan nimiketunnukseen. Virhe voi tapahtua esimerkiksi silloin, kun tilaukset vahvistetaan tai niiden tilaustyyppiä muutetaan.

> Suunniteltua tilausta %1 ei ole.

## <a name="cause"></a>Syy

Kun järjestelmä vahvistaa tilauksen tai muuttaa sen tyyppiä, sen täytyy harkita nimikkeen olemassa olevia suunniteltuja tilauksia uudelleen, jotta suunniteltu toimitus vastaa kysyntää ja olemassa olevaa toimitusta. Osana tätä prosessia järjestelmä luo nimikkeelle suunnitellut tilaukset uudelleen. Tästä syystä toista suunniteltua tilausta, jota järjestelmä odottaa käsiteltäväksi, ei ole enää olemassa.

## <a name="workaround"></a>Ongelman kiertäminen

Hyväksy tilaukset ennen niiden käsittelemistä. Näin tilauksia ei poisteta, kun järjestelmä käsittelee nimikkeen ensimmäisen tilauksen.
