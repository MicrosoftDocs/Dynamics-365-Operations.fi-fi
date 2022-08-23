---
title: Sähköposti-ilmoitusprofiilin määrittäminen
description: Tässä artikkelissa käsitellään sähköpostin ilmoitusprofiilin luontia Microsoft Dynamics 365 Commercessa.
author: bicyclingfool
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: db6c46d471e3b54982132df3e4819236833cf4a8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292132"
---
# <a name="set-up-an-email-notification-profile"></a>Sähköposti-ilmoitusprofiilin määrittäminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään sähköpostin ilmoitusprofiilin luontia Microsoft Dynamics 365 Commercessa.

Kun luot kanavia, voit määrittää sähköposti-ilmoitusprofiilin. Sähköposti-ilmoitusprofiili määrittää myyntitapahtuman tapahtumat (kuten tilausten luomisen, tilausten pakattujen tapahtumien ja laskutettujen tapahtumien), joista ilmoitukset lähetetään asiakkaille. 

Lisätietoja sähköpostin määrittämisestä on kohdassa [Sähköpostiviestin määrittäminen ja lähettäminen](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).



## <a name="create-an-email-template"></a>Luo sähköpostimalli

Ennen sähköposti-ilmoitustyypin käyttöä on luotava organisaation sähköpostimalli Commerce Headquarters -sovelluksessa jokaiselle halutulle ilmoitustyypille. Tässä mallissa määritetään kullakin tuettavalla kielellä sähköpostien aihe, lähettäjä, oletuskieli ja sähköpostin perusteksti.

Voit luoda sähköpostimallin seuraavien ohjeiden avulla.

1. Siirry siirtymisruudussa kohtaan **Moduulit \> Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Parametrit \> Organisaation sähköpostimallit**.
1. Valitse toimintoruudussa **Uusi**.
1. Anna **Sähköpostitunnus** kentässä tunnus auttamaan tämän mallin tunnistamisessa.
1. Kirjoita **Lähettäjän nimi**-kenttään lähettäjän nimi.
1. Syötä **Sähköpostin kuvaus**-kenttään asianmukainen kuvaus.
1. Kirjoita **Lähettäjän sähköpostiosoite** -kenttään lähettäjän sähköpostiosoite.
1. Valitse **Yleiset**-osasta sähköpostimallin oletuskieli. Oletuskieltä käytetään, kun määritetyllä kielellä ei ole lokalisoitua mallia.
1. Laajenna **Sähköpostiviestin sisältö** -osa ja valitse **Uusi**, kun haluat luoda mallin sisällön. Valitse kunkin sisällön kohteen osalta kieli ja sähköpostiviestin aiherivi. Jos sähköpostiin tulee teksti, varmista, että **Leipäteksti on** -ruutu on valittuna.
1. Valitse toimintoruudussa **Sähköpostiviesti** määrittääksesi sähköpostin leipätekstimallin.

Seuraavassa kuvassa näkyy esimerkkejä sähköpostimallin asetuksista.

![Sähköpostimallin asetukset.](media/email-template.png)

Lisätietoja sähköpostimallien luomisesta on kohdassa [Sähköpostimallien luominen tapahtumille](email-templates-transactions.md). 

## <a name="create-an-email-notification-profile"></a>Sähköpostin ilmoitusprofiilin luominen

Luo sähköposti-ilmoitusprofiili headquartersissa noudattamalla seuraavia ohjeita.

1. Siirry siirtymisruudussa kohtaan **Moduulit \> Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Kaupan sähköposti-ilmoitusprofiili**.
1. Valitse toimintoruudussa **Uusi**.
1. Anna **Sähköposti-ilmoitusprofiili**-kentässä profiilille nimi.
1. Syötä **Kuvaus**-kenttään asianmukainen kuvaus.
1. Aseta **Aktiivinen**-kytkin asentoon **Kyllä**.

## <a name="add-a-notification-type"></a>Lisää ilmoituksen tyyppi

Voit luoda sähköpostitapahtuman seuraavien ohjeiden avulla.

1. Siirry siirtymisruudussa kohtaan **Moduulit \> Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Kaupan sähköposti-ilmoitusprofiili**.
1. Valitse **Vähittäismyynnin sähköposti-ilmoituksen asetukset** -kohdasta **Uusi**.
1. Valitse avattavasta luettelosta asianmukainen **Sähköposti-ilmoitustyyppi**.
1. Valitse yllä luomasi sähköpostimalliryhmä avattavasta **Sähköpostitunnus**-luettelosta.
1. Valitse **Käytössä**-valintaruutu.
1. Valitse toimintoruudussa **Tallenna**.

Seuraavassa kuvassa näkyy esimerkkejä tapahtuman ilmoitusasetuksista.

![Tapahtuman ilmoitusasetukset.](media/email-notification-profile.png)


## <a name="schedule-a-recurring-email-notification-process-job"></a>Toistuvan sähköposti-ilmoitusprosessityön ajoittaminen

Sähköposti-ilmoitusten lähettämistä varten työn **Vähittäismyyntitilauksen sähköposti-ilmoituksen käsittely** on oltava käynnissä.

Voit määrittää headquartersissa erätyön tapahtumasähköpostien lähettämistä varten noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Sähköposti ja ilmoitukset \> Lähetä sähköposti-ilmoitus**.
1. Valitse **Vähittäismyyntitilauksen sähköposti-ilmoituksen käsittely** -valintaikkunassa **Toistuminen**.
1. Valitse **Määritä toistuminen** -valintaruudussa **Ei päättymispäivää**.
1. Valitse **Toistumismalli**-kohdassa **Minuutit** ja määritä sitten **Määrä**-kentän arvoksi **1**. Näillä asetuksilla varmistetaan, että sähköposti-ilmoitukset käsitellään mahdollisimman nopeasti.
1. Palaa **Vähittäismyyntitilauksen sähköposti-ilmoituksen käsittely** -valintaikkunaan valitsemalla **OK**.
1. Viimeistele työn määritys valitsemalla **OK**.

## <a name="next-steps"></a>Seuraavat vaiheet

Ennen kuin voit lähettää viestejä, sinun on määritettävä lähtevä postipalvelu. Lisätietoja on kohdassa [Sähköpostin lähettäminen ja määrittäminen](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="additional-resources"></a>Lisäresurssit

[Sähköpostiviestin määrittäminen ja lähettäminen](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[Kanavien yleiskatsaus](channels-overview.md)

[Kanava-asetusten edellytykset](channels-prerequisites.md)

[Organisaatiot ja organisaatiohierarkiat – yleiskatsaus](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
