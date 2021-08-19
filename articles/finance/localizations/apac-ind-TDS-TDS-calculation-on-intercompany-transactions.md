---
title: TDS-laskenta konserniyritysten välisille tapahtumille
description: Tässä aiheessa kuvataan prosessia, jota käytetään konserniyritysten välisten tapahtumien Vero vähennettynä lähteissä (TDS) -laskemiseen vaiheittain.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 029a9bcc6fad7bc3348716aadeeda9552a086e5b1a6d08018c1aaced4b241a1d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727246"
---
# <a name="tds-calculation-on-intercompany-transactions"></a>TDS-laskenta konserniyritysten välisille tapahtumille

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan prosessia, jota käytetään konserniyritysten välisten tapahtumien Vero vähennettynä lähteissä (TDS) -laskemiseen vaiheittain.

Kun konsernin sisäinen ostotilaus tai myyntitilaus luodaan, asiakkaalle tai toimittajalle määritettyä TDS-oletusryhmää käytetään TDS-summan laskemiseen. TDS-summa kirjataan palautetuille ostoreskontratileille laskun kirjaamisen jälkeen.

Järjestelmä luo konsernin sisäisen myyntitilauksen tai ostotilauksen automaattisesti alkuperäiselle ostotilaukselle tai myyntitilaukselle. Oletusarvoinen TDS-ryhmä näkyy konsernin sisäisessä tilauksessa, jotta TDS voidaan laskea. Voit muuttaa TDS-ryhmää. Laskun voi kirjata vain, jos konsernin sisäisen tilauksen nettolaskun summa, joka luodaan automaattisesti, vastaa alkuperäisen tilauksen nettolaskun summaa. (Nettosumma on laskun summa, kun TDS on vähennetty.)

Myyntilasku luodaan esimerkiksi 50 000:lle ja siihen liitetään **10 %**:n TDS-ryhmä. Kirjatun laskun summa on 45 000, ja myyntilaskun kirjattu TDS-summa on 5 000. Konsernin sisäiselle myyntitilaukselle luodaan automaattisesti ostotilaus, ja siihen liitetään **10 %**:n TDS-ryhmä. Jos TDS-ryhmä muutetaan **15 %**:iin, laskua ei voi kirjata, koska automaattisesti luodun konsernin sisäisen myyntitilauksen nettolaskun summa ei vastaa alkuperäisen myyntitilauksen nettolaskun summaa.

Järjestelmä kirjaa automaattisesti maksukirjauskansion, joka luodaan konsernin sisäiselle laskulle. Kirjauskansion voi kirjata vain, jos sen nettomaksusumma vastaa alkuperäisen maksukirjauskansion nettomaksusummaa.
