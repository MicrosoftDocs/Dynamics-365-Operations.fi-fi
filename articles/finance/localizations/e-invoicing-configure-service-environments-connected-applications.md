---
title: Palveluympäristöjen ja yhdistettyjen sovellusten konfiguroiminen
description: Tässä artikkelissa on tietoja palveluympäristöjen ja liitettyjen sovellusten konfiguroinnista.
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 8ede98cfad685992bad3fb643ea46d6adcb08487
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269528"
---
# <a name="configure-service-environments-and-connected-applications"></a>Palveluympäristöjen ja yhdistettyjen sovellusten konfiguroiminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja palveluympäristöjen ja liitettyjen sovellusten konfiguroinnista. Tässä prosessissa on kolme vaihetta. Vaihe 1 on pakollinen, ja vaiheet 2 ja 3 ovat valinnaisia.

## <a name="step-1-create-a-service-environment"></a>Vaihe 1: Palveluympäristön luominen

Kun luot palveluympäristön, määritä luettelo käyttäjistä, jotka voivat ottaa siihen käyttöön globalisointitoimintoja. Joissakin tilanteissa voit myös määrittää luettelon ulkoisista sovelluksista, jotka voivat viestiä sähköisen laskutuksen palvelun kanssa. Määritä numerosarjat, jos niitä käytetään skenaarioissasi.

Tämän vaiheen ohjeet: [Palveluympäristöt](e-invoicing-service-environments.md).

## <a name="step-2-add-certificates-and-secrets"></a>Vaihe 2: Lisää varmenteet ja salaiset koodit

Lisää viittaus Microsoft Azure Key Vaultiin sekä salaisuudet, joita voidaan käyttää skenaarioissasi. Tämä vaihe on pakollinen, jos käsittelyputken toimenpiteet käyttävät sertifikaatteja ja salaisuuksia digitaalisiin allekirjoituksiin tai ulkoisten Internet-palveluiden kanssa kommunikoinnissa.

Tämän vaiheen ohjeet: [Asiakkaan varmenteet ja salaiset koodit](e-invoicing-customer-certificates-secrets.md).

## <a name="step-3-configure-connected-applications"></a>Vaihe 3: Liitettyjen sovellusten määrittäminen

Jos haluat määrittää viestinnän Dynamics 365 Finance- tai Dynamics 365 Supply Chain Management -sovellusten ja sähköisen laskutuksen välillä, määritä Finance ja Supply Chain Management muodostamaan kutsu sähköiseen laskutuspalveluun ja valmistelemaan liiketoimintatiedot yhdistetyssä rakenteessa, joka voidaan muuntaa vaadittuun sähköiseen muotoon. Sovellusten on käsiteltävä myös palvelun vastaukset oikein. Voit tehdä tämän konfiguraation suoraan Finance- tai Supply Chain Management -ympäristössä tai voit tehdä sen valmiiksi Regulatory Configuration Service (RCS) -palvelussa. Jos suoritat konfiguroinnin RCS:ssä, voit sitten ottaa sen käyttöön Finance- tai Supply Chain Management -ympäristössä. Tässä vaiheessa rekisteröit liitetyn sovelluksen parametrien käyttöönottoa varten.

Tämän vaiheen ohjeet: [Yhdistetyt sovellukset](e-invoicing-connected-applications.md).
