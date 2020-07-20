---
title: Työnkulun työnimikkeiden delegointi
description: Jos aiot olla poissa toimistosta tai et voi muutoin käsitellä työnimikkeitä, voit delegoida tai määrittää työnimikkeesi uudelleen muille käyttäjille.
author: ChrisGarty
manager: AnnBe
ms.date: 06/23/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d98d84b89f1f3322a9c896b74b63a3b6425b13b
ms.sourcegitcommit: 267864eb0dccd6e26d49d280bd4ad1b770a73a77
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/26/2020
ms.locfileid: "3515761"
---
# <a name="delegate-work-items-in-a-workflow"></a>Työnkulun työnimikkeiden delegointi

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a>Työnimikkeen delegointi manuaalisesti

Yksittäinen työnimike voidaan delegoida valitsemalla **delegoida**-asetus **työnkulku**-valikosta, lisäämällä kommentin ja syöttämällä käyttäjän, jolle työ delegoidaan. Määrittää työnimikkeen käyttäjälle, jotta käyttäjä voi suorittaa sen loppuun.

## <a name="manually-delegate-multiple-work-items"></a>Delegoi manuaalisesti useita työnimikkeitä

Useita työnimikkeitä voidaan delegoida yhteen **Minulle määritetyt työnimikkeet** -sivulta. Seuraavat työnkulutyypit soveltuvat joukkodelegointiin: ostosopimuksen hyväksynnän työnkulku, ostotilauksen työnkulku, ostoehdotuksen arvostelu ja toimittajan laskun työnkulku. **Delegoi useita työnimikkeitä** -ominaisuus on oletuksena pois käytöstä, ja sen voi ottaa käyttöön kohdassa **Työtilat > Ominaisuuksien hallinta**. Ota yhteyttä järjestelmänvalvojaasi, jos haluat apua tämän toiminnon käyttöön ottamisessa.
1.  Siirry kohtaan **Yleinen > Yleinen > Työnimikkeet > Minulle määritetyt työnimikkeet**.
2.  Valitse delegoitavat työnimikkeet.
3.  Valitse **Delegoi työnimikkeet** -valikko.
4.  Valitse **Käyttäjä**-kentässä käyttäjä, jolle työnimikkeet delegoidaan.
5.  Selitä **Kommentti**-kentässä, miksi delegoit työnimikkeet.
6.  Viimeistele työnimikkeen delegointi napsauttamalla **Delegoi työnimikkeet** -painiketta.

## <a name="automatically-delegate-work-items"></a>Delegoi työnimikkeet automaattisesti

Jos aiot olla poissa toimistosta tai et muuten ole käytettävissä tiettynä aikana, voit siirtää uusia työnimikkeitä automaattisesti muille käyttäjille käyttämällä **Käyttäjäasetukset**-sivua.

### <a name="set-up-automatic-delegation"></a>Automaattisen delegoinnin määrittäminen
1. Valitse **Yhteiset > Asetukset > Käyttäjän asetukset**.
2. Valitse **Työnkulku**-väli lehti. Varmista, että Delegointi-osa on laajennettu. Luo delegointisäännöt määrittämään, milloin tietyt työnimiketyypit delegoidaan. Tällä tavoin voit määrittää järjestelmän delegoimaan työnimikkeesi automaattisesti muille käyttäjille. Luo delegointisääntö seuraavien ohjeiden avulla.  
3. Valitse **Lisää**.
4. Valitse **Vaikutusalue**-kentässä vaihtoehto.
    - Kaikki – delegoi kaikki sinulle määritetyt työnimikkeet.
    - Moduuli – Delegoi vain tiettyyn työnkulkutyyppiin liittyvät työnimikkeet. Jos valitset tämän vaihtoehdon, työnkulkutyyppi on valittava Nimi-kentässä.
    - Työnkulku – Delegoi vain tiettyyn työnkulkuun liittyvät työnimikkeet. Jos valitset tämän vaihtoehdon, työnkulku on valittava Nimi-kentässä.  
5. Valitse **Delegoi**-kentässä käyttäjä, jolle työnimikkeet delegoidaan. Määritä Alkamispäivämäärä ja -kellonaika- ja Päättymispäivämäärä ja -kellonaika -kenttien avulla, milloin haluat delegoida työnimikkeet automaattisesti.  
6. Anna päivämäärä ja kellonaika **Aloituspäivämäärä ja -kellonaika** -kentässä.
7. Anna päivämäärä ja kellonaika **Päättymispäivämäärä ja -kellonaika** -kentässä.
8. Aktivoi tämä delegointisääntö valitsemalla **Käytössä**-valintaruutu. Jos **Moduuli** on valittu vaikutusalueeksi, moduuli on valittava myös Nimi-kentässä. Jos **Työnkulku** on valittu vaikutusalueeksi, tietty työnkulku on valittava delegoitavaksi myös Nimi-kentässä.  
9. Selitä **Kommentti**-kentässä, miksi delegoit työnimikkeet.

