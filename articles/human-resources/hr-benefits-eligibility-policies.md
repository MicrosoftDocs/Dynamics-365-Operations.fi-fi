---
title: Etukelpoisuuden käytännöt
description: Tässä artikkelissa on tietoja etukelpoisuuden käytännöistä, joiden avulla määritetään tiettyyn etuun oikeutetut henkilöt.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: e0c0aa7eebf32fc404e0519c6068b4427e6b87b2
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465147"
---
# <a name="benefit-eligibility-policies"></a>Etuuskelpoisuuden käytännöt

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa on tietoja etukelpoisuuden käytännöistä, joiden avulla määritetään tiettyyn etuun oikeutetut henkilöt.

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

Sinä määrität säännön laajuuden käytännön sisällä. Esimerkiksi, jos luot edun oikeutussäännön käytäntösääntötyypin, jonka nimi on **Johtokunta**, voit määrittää mikä sääntö on, sen käytännön sisällä. Tässä esimerkissä sääntö voisi ilmoittaa, että johtaja-sanan sisältävä työnimike on sisällytettävä sääntöön. Kun olet määrittänyt säännön tai sääntöjen parametrit, jotka sisältyvät käytäntöön, voit määrittää edun tietyn säännön.






[!INCLUDE[footer-include](../includes/footer-banner.md)]