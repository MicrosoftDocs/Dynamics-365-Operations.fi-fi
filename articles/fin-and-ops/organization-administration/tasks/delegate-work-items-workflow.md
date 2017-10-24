--- 
title: "Työnkulun työnimikkeiden delegointi"
description: "Jos aiot olla poissa toimistosta tai et voi muutoin käsitellä työnimikkeitä, voit delegoida tai määrittää työnimikkeesi uudelleen muille käyttäjille."
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 4765fec0cdce0e2f8859c979ff97d20aa6b20bfa
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="delegate-work-items-in-a-workflow"></a>Työnkulun työnimikkeiden delegointi

[!include[task guide banner](../../includes/task-guide-banner.md)]

Jos aiot olla poissa toimistosta tai et voi muutoin käsitellä työnimikkeitä, voit delegoida tai määrittää työnimikkeesi uudelleen muille käyttäjille. Tämä menettely auttaa määrittämään järjestelmän siten, että työnimikkeesi delegoidaan automaattisesti toiselle käyttäjälle.



Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.


## <a name="set-up-automatic-delegation"></a>Automaattisen delegoinnin määrittäminen
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


