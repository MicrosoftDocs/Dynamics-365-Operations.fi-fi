---
title: Palveluympäristöjen ja yhdistettyjen sovellusten konfiguroiminen
description: Tässä artikkelissa on tietoja palveluympäristöjen ja liitettyjen sovellusten konfiguroinnista.
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c1bb3f784148f04c01223ac4e280a18bacfe0e51
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853219"
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
