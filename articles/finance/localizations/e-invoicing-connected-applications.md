---
title: Sovellukset, joista on muodostettu yhteys
description: Tässä aiheessa selitetään, miten yhdistetyt sovellukset määritetään sähköisessä laskutuksessa.
author: dkalyuzh
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 59b67589139c0ce332716acf998825c6a024bded
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371621"
---
# <a name="connected-applications"></a>Sovellukset, joista on muodostettu yhteys

[!include [banner](../includes/banner.md)]

Liitetyt sovellukset ovat ne Microsoft Dynamics 365 Finance- ja Dynamics 365 Supply Chain Management -esiintymät, joihin haluat ehkä ottaa yhteyttä Regulatory Configuration Services (RCS) -palvelun kautta. Liitettyjen sovellusten avulla voit konfiguroida osan globalisointitoimintoa Financessa ja Supply Chain Managementissa, jotta koko sähköisen laskutuksen skenaario toimisi.

Kun otat käyttöön globalisointitoiminnon, Finance- tai Supply Chain Management -sovellukseen liittyvät määritystiedot voidaan julkaista suoraan RCS:stä asianmukaiseen liitettyyn sovellukseen.

Financen tai Supply Chain Managementin parametrien käytettävyys RCS:ssä on hyödyllistä, jos käytössä on useita sovellusympäristöjä, kuten käyttäjän hyväksynnän testausympäristö (UAT) ja tuotantoympäristöjä, ja haluat säilyttää asetukset yhdenmukaisesti käyttämällä samoja parametreja eri ympäristöissä.

## <a name="create-a-connected-application"></a>Luo yhdistetty sovellus

1. Kirjaudu RCS-tilille.
2. Valitse **Globalisaatio-ominaisuudet**-työtilan **Ympäristö**-osassa **Sähköinen laskutus** -ruutu.
3. Valitse **Ympäristöasetukset**-sivun toimintoruudusta **Yhdistetyt sovellukset**.
4. Luo yhdistetty sovellus valitsemalla **Uusi**.
5. Syötä **Nimi**-kenttään yhdistettävän sovelluksen nimi.
6. Valitse **Tyyppi**-kentässä **Dynamics 365 Finance**.
7. Syötä **Sovellus**-kenttään yhdistettävän ympäristön URL-osoite.
8. Määritä ympäristön vuokraaja **Vuokraaja**-kentässä.
9. Valitse **Tallenna**.
10. Testaa yhteys ympäristöön valitsemalla toimintoruudussa **Tarkista yhteys**. Sulje sitten sivu.

## <a name="link-connected-applications-to-environments"></a>Liitettyjen sovellusten linkittäminen ympäristöihin

1. Valitse **Ympäristöasetus**-sivulla **Uusi**, jos haluat määrittää liitetyn sovelluksen ympäristöön.
2. Valitse **Yhdistetty sovellus** -kentässä yhdistetty sovellus.
3. Valitse **Palveluympäristö**-kentässä palveluympäristö.
4. Valitse **Tallenna** ja sulje sitten sivu.
