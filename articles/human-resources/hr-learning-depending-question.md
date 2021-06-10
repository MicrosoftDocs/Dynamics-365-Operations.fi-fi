---
title: Tee kysymys edellisen kysymyksen vastauksen perusteella
description: Ehdollisten kysymysten avulla voit määrittää vastaajalle näkyvän seurantakysymyksen aiemman kysymyksen perusteella.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 39da0418f60273a82cb51e5cf3aad60e4efdb234
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056657"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>Tee kysymys edellisen kysymyksen vastauksen perusteella

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



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



[!INCLUDE[footer-include](../includes/footer-banner.md)]