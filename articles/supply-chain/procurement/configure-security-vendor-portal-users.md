---
title: Toimittajaportaalin käyttäjäsuojaus
description: Tässä artikkelissa käsitellään käyttöoikeuksien määrittämistä Toimittajaportaalia käyttäville ulkoisille toimittajille. Tämän aiheen tiedot koskevat vain Dynamics AX:n helmikuun 2016 ja toukokuun 2016 versioita.
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8e73e9e874fbb8df029e4eccce922a660513c1bf
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568084"
---
# <a name="vendor-portal-user-security"></a>Toimittajaportaalin käyttäjien suojaus

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään käyttöoikeuksien määrittämistä Toimittajaportaalia käyttäville ulkoisille toimittajille. Tämän aiheen tiedot koskevat vain Dynamics AX:n helmikuun 2016 ja 2016 toukokuun versioita.

Toimittajaportaalin toiminnot on korvattu laajennetulla toimittajayhteistyötoiminnallisuudella Dynamics 365 for Operationsin versiossa 1611. Saat lisätietoja toimittajayhteistyön suojauksen määrittämisestä ohjeaiheesta [Toimittajayhteistyön määritys ja ylläpito](set-up-maintain-vendor-collaboration.md). Toimittajaportaali paljastaa rajatun määrän ostotilauksia koskevaa tietoa ulkopuolisille toimittajille. On tärkeää, että määrität toimittajaportaalin käyttöoikeudet oikein Microsoft Dynamics AX:ssä niin, että toimittajilla ei ole liian laajaa pääsyä Dynamics AX:n lisätietoihin. **Tärkeää:** Muista käyttäjistä poiketen, ulkoisilla toimittajilla ei pitäisi olla **Järjestelmänkäyttäjä**-roolia. **Järjestelmänkäyttäjä**-roolille myönnetään oikeuksia, jotka eivät sovellu ulkoisille käyttäjille.

## <a name="setting-up-a-vendor-portal-user"></a>Toimittajaportaalin käyttäjän määrittäminen
Ennen kuin luot käyttäjätilin henkilölle, joka tulee käyttämään Toimittajaportaalia, sinun on määritettävä kyseiselle toimittajalle Toimittajaportaaliyhteistyön salliminen. Käytä **Ostotilausyhteistyö**-kenttää **Yleinen**-välilehdessä **Toimittajat**-sivulla. Ulkoisilla toimittajilla, jotka käyttävät Toimittajaportaalia, on oltava seuraavat asetukset.

-   Microsoft Azure Active Directory (AAD) -käyttäjätili on rekisteröitävä toimittajalle Dynamics AX:n **Käyttäjät**-sivulla.
-   Toimittajalla on oltava **Toimittaja (ulkoinen)** -käyttöoikeusrooli **Järjestelmänkäyttäjä**-roolin sijaan. **Huomautus:** **Järjestelmänkäyttäjä**-rooli myönnetään automaattisesti, kun luot uuden käyttäjätilin Dynamics AX:ssä. Sinun on siksi poistettava kyseinen rooli ja hyväksyttävä saamasi varoitusviesti.
-   Toimittajakäyttäjälle ei pitäisi myöntää oikeutta lisätä kenttiä ostotilaustaulukoista omaan ostotilausnäkymäänsä. Määritä **Mukauttaminen**-välilehden **Käyttäjät** välilehdellä **Eksplisiittinen mukauttaminen sallittu** -vaihtoehto käyttäjälle arvoksi **Ei**.
-   Käyttäjätilin on oltava liitettynä rekisteröityyn yhteyshenkilöön. Valitse **Käyttäjät**-sivulla yhteyshenkilö **Nimi**-kentästä. Valitsemallasi henkilöllä tulisi olla kyseisen toimittajan **Yhteyshenkilö**-rooli.

Jos sama henkilö tarvitsee käyttöoikeudet Toimittajaportaalissa useille toimittajatileille (esimerkiksi eri yrityksille), kunkin kyseisen henkilön käyttäjätilin on oltava liitettynä samaan rekisteröityyn yhteyshenkilöön. **Toimittaja (ulkoinen)** -rooli sisältää kaikki perusominaisuudet, jotka tarvitaan Toimittajaportaalissa satavilla olevien toiminnallisuuksien käyttämiseen. Nämä asetukset auttavat varmistamaan, että ulkoisen käyttäjän näkemä käyttöliittymä näyttää vain halutun skenaarion.

## <a name="additional-resources"></a>Lisäresurssit

[Yhteistyö toimittajien kanssa Toimittajaportaalissa](collaborate-vendors-vendor-portal.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]