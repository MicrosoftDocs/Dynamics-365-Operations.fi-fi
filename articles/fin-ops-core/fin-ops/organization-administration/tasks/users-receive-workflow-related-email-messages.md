---
title: Anna käyttäjille mahdollisuus vastaanottaa työnkulkuun liittyviä sähköpostiviestejä
description: Voit määrittää järjestelmän lähettämään sähköpostiviestejä käyttäjille työnkulkuun liittyvien tapahtumien yhteydessä.
author: jasongre
ms.date: 06/01/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 368fe2fbf1f8a1adcabe37ced5ed942f9fb86fc8
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070422"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a>Anna käyttäjille mahdollisuus vastaanottaa työnkulkuun liittyviä sähköpostiviestejä

[!include [banner](../../includes/banner.md)]


[!INCLUDE [PEAP](../../../../includes/peap-1.md)]

Voit määrittää järjestelmän lähettämään sähköpostiviestejä käyttäjille työnkulkuun liittyvien tapahtumien yhteydessä. Käyttäjille voidaan lähettää esimerkiksi sähköpostiviestejä, kun asiakirjat määritetään heille hyväksyntää varten. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.

1. Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Käyttäjät > Käyttäjät**.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Valitse **toimintoruudussa** **Käyttäjän asetukset**.
4. Valitse **Työnkulku**-väli lehti. Varmista, että **Ilmoitukset**-osa on laajennettu. Voit määrittää **Ilmoitukset**-osassa, miten haluat käyttäjän saavan ilmoituksen työnkulkuun liittyvistä tapahtumista.  
5. Valitse vaihtoehto **Rivinimiketyönkulkutyyppi** -kentässä.
    - Ryhmitelty – nimikkeiden ilmoitukset ryhmitellään yksittäiseen sähköpostiviestiin.
    - Yksilöllinen – sähköpostiviesti lähetetään kullekin rivinimikkeelle.  
    - Jos haluat käyttäjän saavan ilmoituksia asiakasohjelmassa, valitse **Lähetä ilmoitukset sähköpostitse** -valintaruutu.  
6. Valitse **Tallenna**.
7. Sulje sivu.

> [!NOTE]
> Työnkulun sähköpostimallit ovat peräisin joko järjestelmän sähköpostimalleista tai organisaation sähköpostimalleista sen mukaan, onko työnkulku järjestelmätason (ei yrityskohtainen) vai organisaatiotason (yrityskohtainen) työnkulku.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]