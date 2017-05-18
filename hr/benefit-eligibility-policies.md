---
title: "Etukelpoisuuden käytännöt"
description: "Tässä artikkelissa on tietoja etukelpoisuuden käytännöistä, joiden avulla määritetään tiettyyn etuun oikeutetut henkilöt."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 076b4f14a09698b6a0e2f5f3dd4f74ef5b673a8d
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="benefit-eligibility-policies"></a>Etukelpoisuuden käytännöt

[!include[banner](includes/banner.md)]


Tässä aiheessa on tietoja etukelpoisuuden käytännöistä, joiden avulla määritetään tiettyyn etuun oikeutetut henkilöt.

Luodessasi etuja, voit päättää mitkä edut ovat saatavilla kullekin työntekijälle. Seuraavassa taulukossa on esimerkkejä eduista, joita voisit antaa käytettäväksi tietyille työntekijöille.

| Etu          | Kenelle etu on käytettävissä |
|------------------|---------------------------------|
| Sairasvakuutus | Kaikki työntekijät                   |
| Matkapuhelin     | Myyntihekilökunta, johtokunta         |
| Pysäköintiliput   | Johto                      |

Seuraavia osia käytetään luomaan oikeutussääntöjä:

-   Käytäntösäännön tyypit
-   Etukelpoisuuden käytännöt

Käytäntösääntötyypit määrittävät kyselyn parametrit, joiden avulla voit kehittää tiettyjä käytäntösääntöjä. Luotuasi käytäntösääntötyypit, voit luoda etu oikeutussääntökäytäntöjä. Käytäntöjen avulla voit luoda ryhmän sääntöjä, jotka koskevat yhtä tai useampaa yritystä. Jokaisessa käytännössä voit tarkastella mitä vain aiemmin luomistasi edun oikeutussääntötyypeistä. 

Sinä määrität säännön laajuuden käytännön sisällä. Esimerkiksi, jos luot edun oikeutussäännön käytäntösääntötyypin, jonka nimi on **Johtokunta**, voit määrittää mikä sääntö on, sen käytännön sisällä. Tässä esimerkissä sääntö saattaa merkitä, että kaikki ammattinimikkeet, jotka sisältävät sanan "johtaja" sisällytetään sääntöön. Kun olet määrittänyt säännön tai sääntöjen parametrit, jotka sisältyvät käytäntöön, voit määrittää edun tietyn säännön.

<a name="see-also"></a>Lisätietoja
--------

[Etuohjelman määrittäminen ja hallinta](manage-benefit-program.md)




