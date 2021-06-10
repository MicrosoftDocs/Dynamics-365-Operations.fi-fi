---
title: Joustopisteohjelmien määrittäminen
description: Microsoft Dynamics 365 Human Resourcesin joustopisteohjelmien avulla voit rekisteröidä työntekijät etuuksien mukaan ennalta määrätyn määrän joustavia pisteitä.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitCreditPrograms, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1dba179e47f586d7fe689b4a021eb9003eb0d9fc
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051854"
---
# <a name="set-up-flex-credit-programs"></a>Joustopisteohjelmien määrittäminen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resourcesin joustopisteohjelmien avulla voit rekisteröidä työntekijät etuuksien mukaan ennalta määrätyn määrän joustavia pisteitä. Työntekijät voivat valita, miten he kohdistavat joustopisteensä. Jos työntekijä esimerkiksi kuuluu puolisonsa terveyenhoitosuunnitelman piiriin, hän saattaa haluta käyttää muuten terveydenhoitoon käyttämänsä pisteet muihin etuihin. 

1. Valitse **Etujen hallinta** -työtilassa **Suunnitelmat**-kohdasta **Joustopisteohjelmat**.

2. Valitse **Uusi**.

3. Määritä seuraavien kenttien arvot.

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Etuhyvityksen tunnus** | Joustavien pisteiden ohjelman yksilöllinen tunnus. |
   | **Kuvaus** | Joustavien pisteiden ohjelman kuvaus. | 
   | **Päivämäärästä** | Päivämäärä ja aika, jolloin joustavien pisteiden ohjelma tulee voimaan. |
   | **Päivämäärään** | Joustavien pisteiden järjestelmän päättymispäivä. Voit jättää säilyttää oletusarvon (12/31/2154) osoittamaan, että joustavien pisteiden järjestelmän päättymispäivää ei ole aikataulutettu. |
   | **Hyvityksen arvo yhteensä** | Niiden pisteiden määrä, joka jokaisella työntekijällä on käytettävissään etujaan varten. |
   | **Suhteellisen jaon sääntö** | Sääntö, jota käytetään joustavien pisteiden suhteelliseen laskentaan, kun työntekijä palkataan keskellä joustavien pisteiden jaksoa. </br></br><ul><li>**Ei yhtään** – Työntekijä ei saa joustavia pisteitä, jos hänet palkataan joustavien pisteiden ohjelmajakson alkamisen jälkeen.</li><li>**Täydet pisteet** – Työntekijä saa täyden määrän joustavia pistetiä riippumatta hänen palkkaushetkestään.</li><li>**Suhteellinen** – Työntekijä saa aloituspäiväänsä perustuvan suhteellisen määrän joustavia pisteitä.</li></ul> |
   | **Joustavien pisteiden suhteellisen laskennan kaava** | Sääntö, jota käytetään joustavien pisteiden suhteelliseen laskentaan, kun työntekijä palkataan keskellä joustavien pisteiden ohjelman etuusjaksoa. Suhteellinen laskenta perustuu työsuhteen alkamispäivään. Tämä kenttä on käytettävissä vain, jos valitset **Suhteellinen** kentässä **Suhteellisuussääntö**. </br></br><ul><li>**Päivittäin** – Laskee työntekijän saamien joustavien pisteiden suhteellisen määrän päivätasolla. Joustavien pisteiden kokonaismäärä jaetaan jakson päivien määrällä. Jos etuusjakso esimerkiksi on 400 päivää, järjestelmä jakaa joustavien pisteiden kokonaismäärän luvulla 400 laskeakseen työntekijöiden päivittäin saamien joustavien pisteiden määrän.</li><li>**Kuluva kuukausi** – Laskee työntekijän saamien joustavien pisteiden suhteellisen määrän kuukausitasolla kuluvaan kuukauteen pyöristettynä. Joustavien pisteiden kokonaismäärä jaetaan jakson kuukausien määrällä. Jos etuusjakso esimerkiksi on 15 kuukautta, järjestelmä jakaa joustavien pisteiden kokonaismäärän luvulla 15 laskeakseen työntekijöiden kuukausittain saamien joustavien pisteiden määrän.</li><li>**Seuraava kuukausi** – Laskee työntekijän saamien joustavien pisteiden suhteellisen määrän kuukausitasolla seuraavaan kuukauteen pyöristettynä. Joustavien pisteiden kokonaismäärä jaetaan jakson kuukausien määrällä. Jos etuusjakso esimerkiksi on 15 kuukautta, järjestelmä jakaa joustavien pisteiden kokonaismäärän luvulla 15 laskeakseen työntekijöiden kuukausittain saamien joustavien pisteiden määrän.</li></ul> |
   


[!INCLUDE[footer-include](../includes/footer-banner.md)]