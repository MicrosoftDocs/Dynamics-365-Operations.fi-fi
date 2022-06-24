---
title: Yhdistetyt sovellukset
description: Tässä artikkelissa selitetään, miten yhdistetyt sovellukset määritetään sähköisessä laskutuksessa.
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
ms.openlocfilehash: 7a0a9c19009c49b80ca8c182c31592c1a713a2aa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906284"
---
# <a name="connected-applications"></a>Yhdistetyt sovellukset

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
