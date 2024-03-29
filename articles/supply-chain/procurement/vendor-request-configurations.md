---
title: Toimittajapyynnön konfiguroinnit
description: Tässä artikkelissa käsitellään kenttiä, jotka on täytettävä uudessa toimittajapyynnössä.
author: GalynaFedorova
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 0f583caaaf4909918fafc0e8ef08490e25057561
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890854"
---
# <a name="vendor-request-configurations"></a>Toimittajapyynnön konfiguroinnit
[!include [banner](../includes/banner.md)]

Toimittajapyynnön viimeistely edellyttää, että toimittajan yhteyshenkilö suorittaa ohjatun mahdollisen toimittajan rekisteröintitoiminnon.

Voit luoda **Toimittajapyynnön konfiguroinnit** -lomakkeessa profiileja, jotka määrittävät pakolliset ja näkyvät kentät ohjatussa mahdollisen toimittajan rekisteröintitoiminnossa.

Ohjattu toimittajan rekisteröintitoiminto kysyy aluksi mahdollisen toimittajan käyttäjältä, missä maassa tai millä alueella toimittaja harjoittaa liiketoimintaa. Tämä tieto määrittää käytettävän konfiguroinnin. Jos maalle tai alueelle ei ole määritettyä tiettyä konfigurointia, käytetään oletuskonfigurointia.

### <a name="set-up-a-vendor-request-configuration"></a>Toimittajapyynnön konfiguroinnin määrittäminen

Toimittajapyynnön konfiguroinnit -lomakkeessa on oletusarvoisesti käytössä toimittajakonfigurointi.

Oletuskonfiguroinnin maata tai alueita ei voi valita, joten **Maat/alueet**-osaa ei voi muuttaa.

1. Valitse ensin **Hankinta** > **Asetukset** > **Toimittajat** ja sitten **Toimittajapyynnön konfiguroinnit**.
2. Määritä luettelon kenttien tila napsauttamalla **Kentät**-välilehteä.
3. Piilotettu (ei näy)
4. Näytetty (näkyvissä mutta ei pakollinen)
5. Pakollinen (näkyvissä ja pakollinen)
6. Määritä **Sisältö**-välilehdessä, näytetäänkö teksti ohjatussa toiminnossa ja onko ilmoitettava, että mahdollisen toimittajan käyttäjän on hyväksyttävä se ennen siirtymistä ohjatun toiminnon seuraavaan vaiheeseen. Hyväksyntä pyydetään kaikille ehdoille, jotka käyttäjän on hyväksyttävä ennen jatkamista.

Voit antaa lisäksi vahvistussanoman, joka näytetään, kun ohjattu toiminto on valmis. Voit myös lisätä yhden kyselylomakkeen tai useita lomakkeita.

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a>Tietyn maan tai alueen toimittajakonfiguroinnin luonti
1.  Valitse ensin **Hankinta** > **Asetukset** > **Toimittajat** ja sitten **Toimittajapyynnön konfiguroinnit**.
2.  Luo uusi konfigurointi valitsemalla **Uusi** ja nimeä konfigurointi.
3.  Valitse **Tallenna**.
4.  Avaa **Maa/alueet**-välilehti ja valitse maa tai alue, jossa konfigurointia on käytettävä.
5.  Viimeistele konfigurointi noudattamalla oletuskonfiguroinnin ohjeita.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]