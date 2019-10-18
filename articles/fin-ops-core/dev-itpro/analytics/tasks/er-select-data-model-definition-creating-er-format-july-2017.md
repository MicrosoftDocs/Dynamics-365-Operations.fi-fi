---
title: Valitse tietomallin määritykset luodessasi muotoja
description: ER Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen tämän menettelyn vaiheiden suorittamista.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66b9636f6d9da06f0ea65ab311dd9308ff6ae020
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184712"
---
# <a name="select-data-model-definitions-when-you-create-formats"></a>Valitse tietomallin määritykset luodessasi muotoja

[!include [task guide banner](../../includes/task-guide-banner.md)]

ER Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen tämän menettelyn vaiheiden suorittamista. 

Tässä menettelyssä kerrotaan, miten mallin juurinimike voidaan valita tietomallin määritelmäksi, kun sähköisten asiakirjojen luomista varten suunniteltu sähköisen raportoinnin (ER) muotokonfiguraatio lisätään. Tässä menettelyssä lisätään uusi ER-muotokonfiguraatio malliyritykselle Litware Inc. 

Nämä ohjeet on tarkoitettu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli. Vaiheet voidaan suorittaa minkä tahansa tietojoukon avulla.

1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
    * Varmista, onko Litware, Inc. -malliyrityksen konfiguraation lähde käytettävissä ja merkitty aktiiviseksi. Jos konfiguraation lähde ei ole näkyvissä, suorita Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet.  
2. Valitse Raportointikonfiguraatiot.

## <a name="add-a-new-er-data-model-configuration"></a>Uuden ER-tietomallin konfiguraation lisääminen
1. Avaa valintaikkuna napsauttamalla Luo konfigurointi.
    * Lisätään uusi ER-mallin konfiguraatio. Se sisältää tietomallin, joka on tarkoitettu tietolähteeksi ER-raporttien luomisessa.  
2. Syötä Nimi-kenttään Maksumalli (kuvitteellinen).
    * Maksumalli (kuvitteellinen)  
3. Valitse Luo konfiguraatio.
4. Valitse Suunnittelutoiminto.
    * Avaa ER-suunnitteluohjelma ja määritä tämän konfiguraation tietomallin rakenne.  
    * Oletetaan, että suunnittelemme maksujen liiketoimintatoimialueelle tietomallin, joka tukee kahta maksutapaa: tilisiirto ja suoraveloitus.  
5. Avaa valintaikkuna valitsemalla Uusi.
6. Syötä Nimi-kenttään Maksut – tilisiirto.
    * Maksut – tilisiirto  
7. ValitseLisää.
8. Avaa valintaikkuna valitsemalla Uusi.
9. Kirjoita Uusi solmu muodossa -kenttään "Mallin juuri".
10. Syötä Nimi-kenttään Maksut – suoraveloitus.
    * Maksut – suoraveloitus  
11. ValitseLisää.
12. Valitse Tallenna.
13. Sulje sivu.
14. Voit muuttaa tilaa valitsemalla Muuta.
    * Tee mallin luonnosversio valmiiksi, jotta se on uusien mallien yhdistämismääritysten ja muotojen käytettävissä.  
15. Valitse Valmis.
16. Valitse OK.

## <a name="start-to-enter-a-new-er-format-configuration"></a>Aloita syöttämällä uusi ER-muotokonfiguraatio
1. Avaa valintaikkuna napsauttamalla Luo konfigurointi.
2. Anna Uusi-kenttään Muoto perustuu tietomallin maksumalliin (kuvitteellinen).
3. Anna tai valitse Tietomallin määritelmä -kentän arvo.
    * Ota huomioon, että kaikki valitun tietomallin juurinimikkeet ovat tällä hetkellä valittavissa tietomallin määritelmäksi. Voit jatkaa muodon suunnittelua käyttämällä mitä tahansa tietomallin pakollista juurinimikettä. Valitun juurinimikkeen puuttuva mallin yhdistämismääritys ei estä jatkamasta.  
4. Sulje sivu.

## <a name="add-a-new-er-model-mapping-configuration"></a>Uuden ER-mallin yhdistämismäärityksen konfiguraation lisääminen
1. Avaa valintaikkuna napsauttamalla Luo konfigurointi.
2. Anna Uusi-kenttään Mallin yhdistämismääritys perustuu tietomallin maksumalliin (kuvitteellinen).
3. Syötä Nimi-kenttään Maksumallin yhdistämismääritykset (kuvitteellinen).
    * Maksumallin yhdistämismääritykset (kuvitteellinen)  
4. Anna tai valitse Tietomallin määritelmä -kentän arvo.
5. Valitse Luo konfiguraatio.

## <a name="design-er-model-mappings"></a>ER-mallin yhdistämismääritysten suunnittelu
1. Valitse Suunnittelutoiminto.
    * Määritä pakollisten juurinimikkeiden mallien yhdistämismääritykset ER-suunnitteluohjelman avulla.  
2. Valitse Suunnittelutoiminto.
    * Simuloi valitun mallin yhdistämismäärityksen asetus valitun mallin juurinimikkeelle.  
3. Valitse puussa Dynamics 365 for Operations\Table records.
4. Valitse Lisää juuri.
5. Kirjoita Nimi -kenttään Kirjanpito.
6. Syötä Taulu-kenttään LedgerJournalTrans.
    * LedgerJournalTrans  
7. Valitse OK.
8. Valitse Tallenna.
9. Sulje sivu.
10. Sulje sivu.

## <a name="start-to-enter-another-new-er-format-configuration"></a>Aloita syöttämällä toinen ER-muotokonfiguraatio
1. Valitse puussa Payment model (fictitious).
2. Avaa valintaikkuna napsauttamalla Luo konfigurointi.
3. Anna Uusi-kenttään Muoto perustuu tietomallin maksumalliin (kuvitteellinen).
4. Anna tai valitse Tietomallin määritelmä -kentän arvo.
    * Ota huomioon, että nyt sovelluksen tietolähteisiin yhdistettäviä juurinimikkeitä on käytettävissä vain yksi. Kun vähintään yksi mallin yhdistämismääritys on esitelty, vain sovelluksen tietolähteisiin yhdistettyjä mallin juurinimikkeitä voi valita mallin määritelmäksi ER-muodon lisäyksen yhteydessä.   
5. Sulje sivu.
