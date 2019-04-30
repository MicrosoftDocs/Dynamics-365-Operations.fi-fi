---
title: Työnkulun työnimikkeiden delegointi
description: Jos aiot olla poissa toimistosta tai et voi muutoin käsitellä työnimikkeitä, voit delegoida tai määrittää työnimikkeesi uudelleen muille käyttäjille.
author: jasongre
manager: AnnBe
ms.date: 04/09/2019
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
ms.openlocfilehash: feace647d7acef6abf86b13fcb8019c622c55ff6
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/12/2019
ms.locfileid: "976778"
---
# <a name="delegate-work-items-in-a-workflow"></a>Työnkulun työnimikkeiden delegointi

[!include [task guide banner](../../includes/task-guide-banner.md)]

## <a name="manually-delegate-a-work-item"></a>Työnimikkeen delegointi manuaalisesti

Yksittäinen työnimike voidaan delegoida valitsemalla **delegoida**-asetus **työnkulku**-valikosta, lisäämällä kommentin ja syöttämällä käyttäjän, jolle työ delegoidaan. Määrittää työnimikkeen käyttäjälle, jotta käyttäjä voi suorittaa sen loppuun.

## <a name="automatically-delegate-work-items"></a>Delegoi työnimikkeet automaattisesti

Jos aiot olla poissa toimistosta tai et muuten ole käytettävissä tiettynä aikana, voit siirtää uusia työnimikkeitä automaattisesti muille käyttäjille käyttämällä **Käyttäjäasetukset**-sivua.

### <a name="set-up-automatic-delegation"></a>Automaattisen delegoinnin määrittäminen
1. Valitse Yleinen > Asetukset > Käyttäjän asetukset.
2. Valitse Työnkulku-välilehti.
    * Varmista, että Delegointi-osa on laajennettu.    Luo delegointisäännöt määrittämään, milloin tietyt työnimiketyypit delegoidaan. Tällä tavoin voit määrittää järjestelmän delegoimaan työnimikkeesi automaattisesti muille käyttäjille. Luo delegointisääntö seuraavien ohjeiden avulla.  
3. ValitseLisää.
4. Valitse Vaikutusalue-kentässä vaihtoehto.
    * Kaikki – delegoi kaikki sinulle määritetyt työnimikkeet.    Moduuli – Delegoi vain tiettyyn työnkulkutyyppiin liittyvät työnimikkeet. Jos valitset tämän vaihtoehdon, työnkulkutyyppi on valittava Nimi-kentässä.    Työnkulku – Delegoi vain tiettyyn työnkulkuun liittyvät työnimikkeet. Jos valitset tämän vaihtoehdon, työnkulku on valittava Nimi-kentässä.  
5. Valitse Delegoi-kentässä käyttäjä, jolle työnimikkeet delegoidaan.
    * Määritä Alkamispäivämäärä ja -kellonaika- ja Päättymispäivämäärä ja -kellonaika -kenttien avulla, milloin haluat delegoida työnimikkeet automaattisesti.  
6. Anna päivämäärä ja kellonaika Aloituspäivämäärä ja -kellonaika -kentässä.
7. Anna päivämäärä ja kellonaika Päättymispäivämäärä ja -kellonaika -kentässä.
8. Aktivoi tämä delegointisääntö valitsemalla Käytössä-valintaruutu.
    * Jos Moduuli on valittu vaikutusalueeksi, moduuli on valittava myös Nimi-kentässä.    Jos Työnkulku on valittu vaikutusalueeksi, tietty työnkulku on valittava delegoitavaksi myös Nimi-kentässä.  
9. Selitä Kommentti-kentässä, miksi delegoit työnimikkeet.

