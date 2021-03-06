---
title: Sähköpostin ilmoitusprofiilin määrittäminen
description: Tässä ohjeaiheessa käsitellään sähköpostin ilmoitusprofiilin luontia Microsoft Dynamics 365 Commercessa.
author: bicyclingfool
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 7504b2b36f6869f90de196bf32c09e7bdd51e7b5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792654"
---
# <a name="set-up-an-email-notification-profile"></a>Sähköposti-ilmoitusprofiilin määrittäminen

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään sähköpostin ilmoitusprofiilin luontia Microsoft Dynamics 365 Commercessa.

Kun luot kanavia, voit määrittää sähköposti-ilmoitusprofiilin. Näin asiakkaille voidaan lähettää sähköposteja erilaisista tapahtumista, kuten tilausten luomisesta, tilausten lähetystilasta ja maksuvirheistä.

Lisätietoja sähköpostin määrittämisestä on kohdassa [Sähköpostiviestin määrittäminen ja lähettäminen](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="create-an-email-notification-profile"></a>Sähköpostin ilmoitusprofiilin luominen

Luo sähköposti-ilmoitusprofiili noudattamalla seuraavia ohjeita.

1. Siirry siirtymisruudussa kohtaan **Moduulit \> Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Kaupan sähköposti-ilmoitusprofiili**.
1. Napsauta Toimintoruudussa **Uusi**.
1. Anna **Sähköposti-ilmoitusprofiili**-kentässä profiilille nimi.
1. Syötä **Kuvaus**-kenttään asianmukainen kuvaus.
1. Aseta **Aktiivinen**-kytkin asentoon **Kyllä**.

### <a name="create-an-email-template"></a>Luo sähköpostimalli

Ennen sähköposti-ilmoitustyypin käyttöä on luotava organisaation sähköpostimalli Commerce Headquarters -sovelluksessa. Tässä mallissa määritetään kullakin tuettavalla kielellä sähköpostien aihe, lähettäjä, oletuskieli ja sähköpostin perusteksti.

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

![Sähköpostimallin asetukset](media/email-template.png)

### <a name="create-an-email-event"></a>Luo sähköpostitapahtuma

Voit luoda sähköpostitapahtuman seuraavien ohjeiden avulla.

1. Siirry siirtymisruudussa kohtaan **Moduulit \> Vähittäismyynti ja kauppa \> Pääkonttorin asetukset \> Kaupan sähköposti-ilmoitusprofiili**.
1. Etsi haluamasi tietue luettelosta ja valitse se. 
1. Valitse sähköpostimalliryhmän avattavasta **Sähköpostitunnus**-luettelosta.
1. Valitse avattavasta luettelosta asianmukainen **Sähköposti-ilmoitustyyppi**.
1. Valitse **Käytössä**-valintaruutu.
1. Valitse toimintoruudussa **Tallenna**.

Seuraavassa kuvassa näkyy esimerkkejä tapahtuman ilmoitusasetuksista.

![Tapahtuman ilmoitusasetukset](media/email-notification-profile.png)

### <a name="next-steps"></a>Seuraavat vaiheet

Ennen kuin voit lähettää viestejä, sinun on määritettävä lähtevä postipalvelu ja määritettävä erätyö. Lisätietoja on kohdassa [Sähköpostin lähettäminen ja määrittäminen](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).


## <a name="additional-resources"></a>Lisäresurssit

[Sähköpostiviestin määrittäminen ja lähettäminen](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[Kanavien yleiskatsaus](channels-overview.md)

[Kanava-asetusten edellytykset](channels-prerequisites.md)

[Organisaatiot ja organisaatiohierarkiat – yleiskatsaus](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
