---
title: "Luo ja käsittele määritysten noudattaminen"
description: "Tällä menettelyllä voi hallita määrityksistä poikkeamisia aiemmin luodun laatutilauksen perusteella."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 4082caf2cc8393345d4f79a991f2cf205b06b142
ms.contentlocale: fi-fi
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-process-a-conformance"></a>Luo ja käsittele määritysten noudattaminen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tällä menettelyllä voi hallita määrityksistä poikkeamisia aiemmin luodun laatutilauksen perusteella. Voit toistaa tallenteen USMF-esittely-yrityksessä ja käyttää ehdotettuja arvoja. Tämän menettelyn suorittaa yleensä laatuassistentti.  Edellytyksenä on suorittaa Tarkista tavaroiden laatu -tehtävätallenteen suorittaminen. Määrityksistä poikkeamisen hyväksymisen käsittely edellyttää, että tehtävätallenteen suorittajalle on määritetty Nimi-arvo Käyttäjät-sivulla. Asiakirjojen huomautusten käyttö taas edellyttää, että tiedoston käsittely on aktivoitu käyttäjäasetuksissa.


## <a name="select-a-quality-order"></a>Valitse laatutilaus.
1. Valitse Laatutilaukset.
2. Merkitse valittu rivi luettelossa.
    * Valitse Tarkista tavaroiden laatu -tehtävätallenteessa luotu laatutilaus.  

## <a name="create-a-nonconformance"></a>Luo määrityksistä poikkeaminen
1. Valitse Kyselyt.
2. Valitse Määrityksistä poikkeamiset.
3. Valitse Uusi.
4. Avaa haku napsauttamalla Ongelman tyyppi -kentässä avattavan valikon painiketta.
    * Valitse tarkistuksen aikana löytynyt ongelma.  
5. Avaa haku napsauttamalla Ongelman tyyppi -kentässä avattavan valikon painiketta.
6. Etsi haluamasi tietue luettelosta ja valitse se.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Valitse OK.

## <a name="approvereject-a-nonconformance"></a>Hyväksy tai hylkää määrityksistä poikkeaminen
1. Valitse Toiminnot.
2. Valitse Hyväksy määrityksistä poikkeaminen.
    * Hyväksy tässä esimerkissä määrityksistä poikkeamisen. Hyväksytyt määrityksistä poikkeamiset voidaan liittää liittyviin toimintoihin tallentamaan työ, joka tehdään osana määrityksistä poikkeamisen käsittelyä ja, kuten tässä työvaiheessa, korjauskäsittelyn käsittelyä.  
3. Valitse Kyllä.

## <a name="create-a-correction-action"></a>Luo korjaustoiminto
1. Valitse Korjaukset.
2. Valitse Uusi.
3. Merkitse valittu rivi luettelossa.
4. Avaa haku napsauttamalla Henkilöstönumero-kentässä avattavan valikon painiketta.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Klikkaa Valitse.
7. Valitse Liitä.
    * Luo korjausta koskeva huomautus. Tässä esimerkissä toimintona on yhteydenotto toimittajaan ja keskustelu määrityksistä poikkeamistapauksesta.  
8. Valitse Uusi.
9. Valitse Huomautus.
    * Huomaa, että raporttiasetusten mukaan eri asiakirjatyyppejä voi tulostaa raportteihin, jotka liittyvät määrityksistä poikkeamisen hallintaan.  
10. Kirjoita arvo Kuvaus-kenttään.
11. Sulje sivu.

## <a name="maintain-a-correction"></a>Ylläpidä korjausta
1. Valitse Merkitse valmiiksi.
2. Valitse OK.
3. Sulje sivu.

## <a name="close-a-nonconformance"></a>Sulje määrityksistä poikkeaminen
1. Valitse Toiminnot.
2. Valitse Sulje määrityksistä poikkeaminen.
3. Valitse Kyllä.
4. Sulje sivu.
5. Sulje sivu.

