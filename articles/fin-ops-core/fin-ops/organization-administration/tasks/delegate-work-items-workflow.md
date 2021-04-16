---
title: Työnkulun työnimikkeiden delegointi
description: Jos aiot olla poissa toimistosta tai et voi muutoin käsitellä työnimikkeitä, voit delegoida tai määrittää työnimikkeesi uudelleen muille käyttäjille.
author: ChrisGarty
ms.date: 07/07/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed21f6d32cdcf74eb153daba32c20b7cef94d4e4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747366"
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
4. Valitse **Vaikutusalue**-kentässä vaihtoehto:
    - Kaikki – delegoi kaikki sinulle määritetyt työnimikkeet.
    - Moduuli – Delegoi vain tiettyyn työnkulkutyyppiin liittyvät työnimikkeet. Jos valitset tämän vaihtoehdon, työnkulkutyyppi on valittava **Nimi**-kentässä.
    - Työnkulku – Delegoi vain tiettyyn työnkulkuun liittyvät työnimikkeet. Jos valitset tämän vaihtoehdon, työnkulku on valittava **Nimi**-kentässä.  
5. **Nimi**-kentässä:
    - Valitse **moduulin** vaikutusalueeksi kohdemoduuli.
    - Valitse **työnkulun** vaikutusalueeksi kohdetyönkulku.
6. Valitse **Delegoi**-kentässä käyttäjä, jolle työnimikkeet delegoidaan. Määritä **Alkamispäivämäärä ja -kellonaika**- ja **Päättymispäivämäärä ja -kellonaika** -kenttien avulla, milloin haluat delegoida työnimikkeet automaattisesti.  
7. Anna päivämäärä ja kellonaika **Aloituspäivämäärä ja -kellonaika** -kentässä.
8. Anna päivämäärä ja kellonaika **Päättymispäivämäärä ja -kellonaika** -kentässä.
9. Aktivoi tämä delegointisääntö valitsemalla **Käytössä**-valintaruutu. 
10. Selitä **Kommentti**-kentässä, miksi delegoit työnimikkeet.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]