---
title: NF-e-XML-tiedostojen siirtäminen liitteinä
description: Tässä artikkelissa käsitellään NF-e-XML-tiedostojen siirtämistä Microsoft Dynamics 365 Finance- tai Dynamics 365 Supply Chain Management -tietokannasta ja niiden ottamista käyttöön sen sijaan liitteinä.
author: gionoder
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2022-01-27
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: ce9061896759efeb8e8960e84656d5fc1f0616ae
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877894"
---
# <a name="move-nf-e-xml-files-as-attachments"></a>NF-e-XML-tiedostojen siirtäminen liitteinä

[!include [banner](../includes/banner.md)] 


Kun sähköisiä veroasiakirjoja (NF-e) myönnetään, XML-tiedostot luodaan Microsoft Dynamics 365 Finance- ja Dynamics 365 Supply Chain Management -tietokannoissa, joihin ne myös tallennetaan. Brasilian lokalisoinnissa **NF-e-XML-tiedoston siirto liitteenä** -ominaisuuden avulla voi vapauttaa näiden XML-tiedostojen käyttämän tilan tietokannassa.

Ominaisuus siirtää tietyn päivämääräalueen ja veroviranomaisen osalta NF-e-XML-tiedostot Finance- tai Supply Chain Management -tietokannasta Azure-tilauksen Blob-objektisäilöön. Tämä siirron jälkeen tiedostot ovat käytettävissä vain liitteinä. Kun XML-tiedostot on siirretty Blob-objektisäilöön, alkuperäiset tiedostot poistetaan Finance- tai Supply Chain Management -tietokannasta. Näin tietokantaan vapautuu niiden käyttämä tila.

**NF-e-XML-tiedoston siirto liitteenä** -ominaisuus otetaan käyttöön seuraavasti.

1. Avaa **Ominaisuuksien hallinta** -työtila Financessa tai Supply Chain Managementissa.
2. Hae ja valitse **NF-e-XML-tiedoston siirto liitteenä** -ominaisuus **Kaikki**-välilehdessä.
3. Valitse **Ota käyttöön nyt**.

NF-e-XML-tiedostot siirretään liitteinä seuraavasti.

1. Valitse **Myyntireskontra** \> **Veroasiakirjat** \> **Sähköiset veroasiakirjat** \> **Siirrä NF-e-XML-tiedosto liitteinä**.
2. Valitse alkamis- ja päättymispäivämäärät **Päivämäärästä**- ja **Päivämäärään**-kentissä.
3. Anna tai valitse arvo **Veroviranomaisen tunnus** -kenttään.
4. Valitse **OK**.

> [!IMPORTANT]
> Tätä prosessia ei voi peruuttaa. Kun NF-e-XML-tiedostot on siirretty, käyttäjät näkevät ne vain valitsemalla **Liitteet** **Veroasiakirja**-sivun yläosassa.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
