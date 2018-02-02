--- 
title: Tee kysymys edellisen kysymyksen vastauksen perusteella
description: "Ehdollisten kysymysten avulla voit määrittää vastaajalle näkyvän seurantakysymyksen aiemman kysymyksen perusteella."
author: twheeloc
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 05f7af94813934c1d77d6a509587280395f0e8bd
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>Tee kysymys edellisen kysymyksen vastauksen perusteella

[!include[task guide banner](../../includes/task-guide-banner.md)]

Ehdollisten kysymysten avulla voit määrittää vastaajalle näkyvän seurantakysymyksen aiemman kysymyksen perusteella. Jos kysymys on esimerkiksi Pidätkö kahvista vai teestä, looginen seurantakysymys voidaan määrittää sen perusteella, valitseeko vastaaja kahvin vai teen. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.


## <a name="find-the-existing-questionnaire"></a>Aiemmin määritetyn kyselylomakkeen etsiminen
1. Siirry kohtaan Kyselylomake > Suunnittelu > Kyselylomakkeet.
2. Valitse luettelosta WorkFH-kyselylomake.

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a>Kaikkien kysymysten ja alikysymysten lisääminen kyselylomakkeeseen
1. Valitse Kysymykset.
2. Valitse Uusi.
3. Valitse Kysymys-kentässä kysymys numero 00016.
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Valitse Tallenna.
7. Sulje sivu.

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a>Kyselylomakkeen järjestyksen määrittäminen ehdolliseksi ja kysymyksen määrittäminen sopivan vastauksen perusteella
1. Valitse Muokkaa.
2. Laajenna osa Asetukset.
3. Valitse Kysymysjärjestys-kentässä Ehdollinen.
4. Valitse Ehdollinen kysymys.
5. Valitse puussa solmu Questions\Explain why you answered the previous question the way you did?
6. Valitse Ensisijainen kysymys -kentässä kysymys numero 00009
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Syötä Vastaus-kenttään sen vastauksen numerojärjestyksen tunnus, jonka perusteella haluat määrittää kysymyksen. Syötä esimerkiksi 1 ensimmäiselle vastausvaihtoehdolle.
9. Valitse Tallenna.
10. Valitse puussa solmu Questions\I am paid fairly for the work I do.
    * Huomaa, että päivitetyssä kysymyksen puussa näkyy riippuvuus.  


