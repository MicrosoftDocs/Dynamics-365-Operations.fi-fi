---
title: Työnkulun työnimikkeiden delegointi
description: Jos aiot olla poissa toimistosta tai et voi muutoin käsitellä työnimikkeitä, voit delegoida tai määrittää työnimikkeesi uudelleen muille käyttäjille.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aceafbe8dfcdac2ac7b97a4f77a9a30599c60c51
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140579"
---
# <a name="delegate-work-items-in-a-workflow"></a>Työnkulun työnimikkeiden delegointi

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a>Työnimikkeen delegointi manuaalisesti

Yksittäinen työnimike voidaan delegoida valitsemalla **delegoida**-asetus **työnkulku**-valikosta, lisäämällä kommentin ja syöttämällä käyttäjän, jolle työ delegoidaan. Määrittää työnimikkeen käyttäjälle, jotta käyttäjä voi suorittaa sen loppuun.

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

