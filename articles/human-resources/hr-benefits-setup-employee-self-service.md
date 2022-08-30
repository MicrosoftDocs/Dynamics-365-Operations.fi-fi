---
title: Työntekijän itsepalvelun määrittäminen
description: Microsoft Dynamics 365 Human Resources -ohjelmassa voit määrittää ylimmän tason siirtymisruudut työntekijän itsepalvelussa.
author: twheeloc
ms.date: 12/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cdc82c23635cc99c37aa770b996d9d2df43f5059
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324635"
---
# <a name="configure-employee-self-service"></a>Työntekijän itsepalvelun määrittäminen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resourcesissa voidaan määrittää ylimmän tason siirtymisruudut **työntekijän itsepalvelussa**. Etuussuunnitelmaruudut ohjaavat käyttäjät etuussuunnitelmiin, joihin he ovat oikeutettuja.

## <a name="set-up-a-benefit-plans-tile"></a>Etuussuunnitelmien ruudun määrittäminen

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Työntekijän itsepalvelun parametrit**.

2. Valitse **Etuussuunnitelmien ruudun asetukset** -välilehti ja valitse sitten **Uusi**.

3. Määritä seuraavien kenttien arvot.

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Suunnitelman tyypin koodi** | Suunnitelmatyyppi, joka näytetään, kun tämä ruutu on valittu **Etujen itsepalvelu** -ruudusta. |
   | **Ruudun tunnus** | Ruudun yksilöivä tunniste. |
   | **Ruudun selitteen teksti** | Teksti, joka tulee näkyviin **Etujen itsepalvelun** ruudussa. |
   | **Kuvaus** | Ruudun kuvaus. |
   | **Ruudun taustakuva** | Ruudussa käytettävän kuvan URL-osoite (valinnainen). |
   | **Seuraa avointa ilmoittautumista** | Valitse tämä vaihtoehto, kun haluat seurata tämän suunnitelmatyypin avointa rekisteröitymisen etenemistä. Joissakin luoduissa suunnitelmissa on esimerkiksi mahdollista, että **Suunnitelman tyyppi = Muu**. Nämä suunnitelmat saattavat olla valinnaisia suunnitelma, joiden rekisteröitymisen etenemistä ei haluta seurata. Jos tätä suunnitelman tyyppiä ei valita, tämä suunnitelmatyyppi ohitetaan seurattaessa edistymistä tai rekisteröitymisen valmistumista **Avaa rekisteröinti** -välilehdessä. Tämä asetus koskee sitä suunnitelman tyyppiä, joka on valittu kaikille kausille ja kaikkiin yrityksiin. |

4. Valitse **Tallenna**.

## <a name="set-up-a-flex-credit-plan-tile"></a>Joustoluottosuunnitelman ruudun määrittäminen

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Työntekijän itsepalvelun parametrit**.

2. Valitse **Joustoluottosuunnitelman ruudun asetukset** -välilehti ja valitse sitten **Uusi**.

3. Määritä seuraavien kenttien arvot.

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Etuhyvityksen tunnus** | Joustohyvitysohjelmasuunnitelmat, jotka näytetään, kun tämä ruutu valitaan **Etujen itsepalvelu** -ruudusta. |
   | **Ruudun tunnus** | Ruudun yksilöivä tunniste. |
   | **Ruudun selitteen teksti** | Teksti, joka tulee näkyviin **Etujen itsepalvelun** ruudussa. |
   | **Kuvaus** | Ruudun kuvaus. |
   | **Ruudun taustakuva** | Ruudussa käytettävän kuvan URL-osoite (valinnainen). |
   | **Seuraa avointa ilmoittautumista** | Valitse tämä vaihtoehto, kun haluat seurata tämän suunnitelmatyypin avointa rekisteröitymisen etenemistä. Joissakin luoduissa suunnitelmissa on esimerkiksi mahdollista, että **Suunnitelman tyyppi = Muu**. Nämä suunnitelmat saattavat olla valinnaisia suunnitelma, joiden rekisteröitymisen etenemistä ei haluta seurata. Jos tätä suunnitelman tyyppiä ei valita, tämä suunnitelmatyyppi ohitetaan seurattaessa edistymistä tai rekisteröitymisen valmistumista **Avaa rekisteröinti** -välilehdessä. Tämä asetus koskee sitä suunnitelman tyyppiä, joka on valittu kaikille kausille ja kaikkiin yrityksiin. |

4. Valitse **Tallenna**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
