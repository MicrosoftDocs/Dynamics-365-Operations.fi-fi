---
title: Määrityksistä poikkeamisia hyväksyvät työntekijät
description: Tässä aiheessa kuvataan, kuinka määritetään määrityksistä poikkeamisia hyväksyvät työntekijät.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d3f647de2c188661c2c9c5f31e2642c3f8ca0b5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021777"
---
# <a name="workers-responsible-for-approving-nonconformances"></a>Määrityksistä poikkeamisia hyväksyvät työntekijät

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, kuinka määritetään määrityksistä poikkeamisia hyväksyvät työntekijät.

Määrityksistä poikkeamiset on hyväksyttävä, ennen kuin käyttäjät voivat alkaa syöttää tietoja, kuten korjauksia tai työvaiheita. Ennen kuin käyttäjät voivat hyväksyä tai hylätä määrityksistä poikkeamisia, käyttäjätunnus (käyttäjätietue) on linkitettävä työntekijätietueeseen. Voit vaihtoehtoisesti määrittää laadusta vastaavat työntekijät ja sallia sitten yhden työntekijän hyväksyä työt toisen työntekijän puolesta.

## <a name="enable-a-user-for-nonconformance-processing"></a>Salli käyttäjälle määrityksistä poikkeamisen käsittely

Ennen kuin käyttäjä voi hyväksyä tai hylätä määrityksistä poikkeamisia, käyttäjätietue on linkitettävä työntekijätietueeseen. Tämän jälkeen hyväksyntäkentät voidaan määrittää automaattisesti, ja nykyinen käyttäjä voidaan täyttää aikaraportille automaattisesti. Ennen kuin käyttäjä voi käyttää asiakirjojen huomautuksia, tiedoston käsittely on aktivoitava käyttäjäasetuksissa.

1. Valitse **Järjestelmänvalvojat \> Käyttäjät \> Käyttäjät**.
1. Etsi ja avaa käyttäjä, jonka tulisi pystyä hyväksymään tai hylkäämään määrityksistä poikkeamisia.
1. Määritä **Henkilö**-kenttään nykyiseen käyttäjätietueeseen liittyvän työntekijän nimi.
1. Valitse toimintoruudussa **Käyttäjän asetukset**.
1. **Asetukset**-sivulla nykyiselle käyttäjätietueelle **Asetukset**-välilehdessä määritä **Ota tiedoston käsittely käyttöön** -asetukseksi *Kyllä*.
1. Sulje sivut.

## <a name="define-workers-that-are-responsible-for-quality"></a>Määritä laadusta vastaavat työntekijät

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Laadusta vastaavat työntekijät**.
2. Valitse toimintoruudussa **Uusi**.
3. Valitse **Työntekijä**-kentästä työntekijä, joka lisää laatutiedot.
4. Valitse **Vastuussa oleva työntekijä** -kentässä työntekijä, jonka puolesta valittu työntekijä syöttää työt. Kun määrityksistä poikkeamisia luodaan ja päivitetään, työntekijä syötetään oletusarvon mukaan **Työntekijä**-kenttiin.

## <a name="additional-resources"></a>Lisäresurssit

- [Laadunhallinnan yleiskuvaus](quality-management-processes.md)
- [Laadun ja määrityksistä poikkeamisen hallinnan ottaminen käyttöön](enable-quality-management.md)
- [Laadun kulut](quality-charges.md)
- [Määrityksistä poikkeamisia koskevat karanteenivyöhykkeet](quality-quarantine-zones.md)
- [Määrityksistä poikkeamisten diagnostiikkatyypit](quality-diagnostic-types.md)
- [Määrityksistä poikkeamisten laatukulut](quality-charges.md)
- [Toiminnot määrityksistä poikkeamisille](quality-operations.md)
- [Laadunhallinta varastoprosesseja varten](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
