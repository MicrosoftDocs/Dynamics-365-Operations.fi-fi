---
title: Poikkeusten tutkiminen ja selvittäminen
description: Toimittajan laskukäytännöt suoritetaan, kun toimittajan lasku kirjataan Toimittajan lasku -sivun avulla ja kun Toimittajan laskukäytäntöjen rikkeet -sivu avataan.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c6f8c8dcf7a301c7fb2d095658ac96cd4a24dff
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567005"
---
# <a name="researchresolve-exceptions"></a>Poikkeusten tutkiminen ja selvittäminen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Toimittajan laskukäytännöt suoritetaan, kun toimittajan lasku kirjataan Toimittajan lasku -sivun avulla ja kun Toimittajan laskukäytäntöjen rikkeet -sivu avataan. Voit myös määrittää toimittajan laskun työnkulun, kun haluat suorittaa toimittajan laskukäytännöt aina, kun lasku lähetetään työnkulkuun. 

Toimittajan laskukäytännöt eivät koske laskurekisteriin tai laskukirjauskansioon luotuja laskuja. 

Laskun täsmäytyksen vahvistuksessa ei käytetä toimittajan laskukäytäntöjä, vaan Ostoreskontran parametrit -määritettyjä käytäntöjä.

Tässä tallenteessa käytetään esittely-yritystä USMF. Nämä vaiheet suorittaa ostoreskontran esimies tai laskentapäällikön rooli. Varmista ennen aloittamista, että laskun täsmäytyksen konfigurointiavain on valittuna.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Toimittajan laskujen käytäntöjen luomisen valmisteleminen
1. Siirry kohtaan Ostoreskontra > Asetukset > Ostoreskontran parametrit.
2. Valitse Laskun oikeellisuustarkistus -välilehti.
3. Valitse Päivitetäänkö laskun otsikon tila automaattisesti -valintaruutu tai poista sen valinta.
4. Valitse OK.
5. Valitse Kirjaa lasku, jossa on ristiriitoja -kentässä vaihtoehto.
6. Sulje sivu.
7. Siirry kohtaan Ostoreskontra > Käytännön asetukset > Toimittajan laskukäytännöt.
8. Valitse Parametrit.
9. Valitse btnAdd.
10. Sulje sivu.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Toimittajan laskujen käytäntösääntöjen tyyppien luominen
1. Siirry kohtaan Ostoreskontra > Käytännön asetukset > Toimittajan laskutuskäytännön sääntötyypit.
2. Valitse Uusi.
3. Kirjoita arvo Säännön nimi-kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Avaa haku valitsemalla Kyselyn nimi -kentässä avattavan valikon painike.
6. Etsi haluamasi tietue luettelosta ja valitse se.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Valitse Tallenna.
9. Sulje sivu.

## <a name="define-a-vendor-invoice-policy"></a>Toimittajan laskujen käytännön määrittäminen
1. Siirry kohtaan Ostoreskontra > Käytännön asetukset > Toimittajan laskukäytännöt.
2. Valitse Uusi.
3. Kirjoita arvo Nimi-kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Laajenna tai tiivistä Käytännön organisaatiot -osa.
6. Valitse puussa solmu Contoso Entertainment System USA.
7. ValitseLisää.
8. Laajenna tai tiivistä Käytäntösäännöt-osa.
9. Valitse Luo käytäntösääntö.
10. Kirjoita Käytäntösääntö-kenttään arvo.
11. Valitse Suodatin.
12. ValitseLisää.
13. Merkitse valittu rivi luettelossa.
14. Avaa haku valitsemalla Taulu-kentässä avattavan valikon painike.
15. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
16. Avaa haku valitsemalla Johdettu taulu -kentässä avattavan valikon painike.
17. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
18. Avaa haku valitsemalla Kenttä-kentässä avattavan valikon painike.
19. Kirjoita arvo Kenttä-kenttään.
20. Sulje sivu.
21. Kirjoita arvo Ehdot-kenttään.
22. Valitse OK.
23. Valitse OK.
24. Sulje sivu.
25. Sulje sivu.

