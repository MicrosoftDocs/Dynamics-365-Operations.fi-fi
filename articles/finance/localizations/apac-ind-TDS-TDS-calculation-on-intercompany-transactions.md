---
title: TDS-laskenta konserniyritysten välisille tapahtumille
description: Tässä aiheessa kuvataan prosessia, jota käytetään konserniyritysten välisten tapahtumien Vero vähennettynä lähteissä (TDS) -laskemiseen vaiheittain.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 381b00c64e3e3a09a245c82cbe1f1599986a49aa
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726974"
---
# <a name="tds-calculation-on-intercompany-transactions"></a>TDS-laskenta konserniyritysten välisille tapahtumille

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan prosessia, jota käytetään konserniyritysten välisten tapahtumien Vero vähennettynä lähteissä (TDS) -laskemiseen vaiheittain.

Kun konsernin sisäinen ostotilaus tai myyntitilaus luodaan, asiakkaalle tai toimittajalle määritettyä TDS-oletusryhmää käytetään TDS-summan laskemiseen. TDS-summa kirjataan palautetuille ostoreskontratileille laskun kirjaamisen jälkeen.

Järjestelmä luo konsernin sisäisen myyntitilauksen tai ostotilauksen automaattisesti alkuperäiselle ostotilaukselle tai myyntitilaukselle. Oletusarvoinen TDS-ryhmä näkyy konsernin sisäisessä tilauksessa, jotta TDS voidaan laskea. Voit muuttaa TDS-ryhmää. Laskun voi kirjata vain, jos konsernin sisäisen tilauksen nettolaskun summa, joka luodaan automaattisesti, vastaa alkuperäisen tilauksen nettolaskun summaa. (Nettosumma on laskun summa, kun TDS on vähennetty.)

Myyntilasku luodaan esimerkiksi 50 000:lle ja siihen liitetään **10 %**:n TDS-ryhmä. Kirjatun laskun summa on 45 000, ja myyntilaskun kirjattu TDS-summa on 5 000. Konsernin sisäiselle myyntitilaukselle luodaan automaattisesti ostotilaus, ja siihen liitetään **10 %**:n TDS-ryhmä. Jos TDS-ryhmä muutetaan **15 %**:iin, laskua ei voi kirjata, koska automaattisesti luodun konsernin sisäisen myyntitilauksen nettolaskun summa ei vastaa alkuperäisen myyntitilauksen nettolaskun summaa.

Järjestelmä kirjaa automaattisesti maksukirjauskansion, joka luodaan konsernin sisäiselle laskulle. Kirjauskansion voi kirjata vain, jos sen nettomaksusumma vastaa alkuperäisen maksukirjauskansion nettomaksusummaa.
