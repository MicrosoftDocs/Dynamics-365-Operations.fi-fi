---
title: Luo puhelinkeskustilauksia
description: Tässä menettelyssä esitellään asiakkaan etsiminen, uuden tilauksen luominen, tuotteen hakeminen ja maksun periminen asiakkaalta.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c875eaa85d9da997b75b296ad9ace99ae1e91798
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594233"
---
# <a name="create-call-center-orders"></a>Luo puhelinkeskustilauksia

[!include [banner](../includes/banner.md)]

Tässä menettelyssä esitellään asiakkaan etsiminen, uuden tilauksen luominen, tuotteen hakeminen ja maksun periminen asiakkaalta. Tässä menettelyssä käytetään esittely-yritystä USRT. Tämä on tarkoitettu myyntitilauksia käsittelevälle assistentille. Edellytykset: Menettelyn suorittava käyttäjä on määritetty puhelinkeskuksen käyttäjiksi. Julkaistussa Fabrikamin puolivuosittaisessa luettelossa on vähintään yksi lähdekoodi.

1. Valitse **Retail ja Commerce \> Asiakkaat \> Asiakaspalvelu**.
2. Anna **SearchText**-kenttään hakuehdot, joilla etsit asiakasta.
    * Valitse tässä esimerkissä menettelytyypiksi Nieminen ja valitse **sarkainnäppäin**.  
3. Valitse Haku.
    * Koska esittelytiedoissa on vain yksi asiakas nimeltä Nieminen, hänet valitaan automaattisesti.  
4. Valitse **Uusi myyntitilaus**.
5. Laajenna tai tiivistä **myyntitilauksen** otsikko-osa.
6. Valitse luettelon lähdekoodi.
    * Jos aktiivisia lähdekoodeja ei ole, voit ohittaa tämän vaiheen.  
7. Valitse **Lisää rivi**.
8. Anna **Nimiketunnus**-kenttään nimikkeen hakuehto.
    * Anna tässä mallimenettelyssä osittainen nimikenumero 8111 ja paina sarkainnäppäintä. Toiminto avaa nimikkeen hakuikkunan.  
9. Valitse myyntitilaukseen lisättävä tuote.
10. Syötä myyntimäärä.
11. Valitse **Luo**.
12. Valitse **Valmis**, kun haluat tarkistaa asiakkaan maksun.
13. Valitse **Lisää**.
    * Lisää-linkki löytyy Maksut-välilehdestä. Laajenna Maksut-välilehti, jos se on tiivistetty.  
14. Valitse maksutapa.
    * Valitse tässä menettelyssä käteismaksutapa.  
15. Sulje sivu.
16. Anna määrä.
    * Anna tässä menettelyssä tilaussummaksi summa, joka löytyy Myyntitilauksen yhteenveto -sivun summakentän vasemmalta puolelta. Tällä toiminnolla voi määrittää tilauksen kokonaan maksetuksi.  
17. Valitse **OK**.
18. Valitse **Lähetä**.

## <a name="additional-resources"></a>Lisäresurssit

[Tapahtumasähköpostien mukauttaminen toimitustilan mukaan](../customize-email-delivery-mode.md)

[Toimitustavan muuttaminen myyntipisteessä](../pos-change-delivery-mode.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]