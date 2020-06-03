---
title: Luo ja käsittele määritysten noudattaminen
description: Tässä aiheessa kerrotaan, miten voit hallita määrityksistä poikkeamisia aiemmin luodun laatutilauksen perusteella.
author: perlynne
manager: tfehr
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bf20ed737707b7cf99023e3c78489caf4a68eab
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383616"
---
# <a name="create-and-process-a-conformance"></a>Luo ja käsittele määritysten noudattaminen

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kerrotaan, miten voit hallita määrityksistä poikkeamisia aiemmin luodun laatutilauksen perusteella. Voit toistaa tallenteen USMF-esittely-yrityksessä ja käyttää ehdotettuja arvoja. Tämän menettelyn suorittaa yleensä laatuassistentti.  Edellytyksenä on suorittaa [Tarkista tavaroiden laatu](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md) -ohjeet. Määrityksistä poikkeamisen hyväksymisen käsittely edellyttää, että tehtävätallenteen suorittajalle on määritetty Nimi-arvo Käyttäjät-sivulla. Asiakirjojen huomautusten käyttö taas edellyttää, että tiedoston käsittely on aktivoitu käyttäjäasetuksissa.


## <a name="select-a-quality-order"></a>Valitse laatutilaus.
1. Valitse siirtymisruudussa **Moduulit > Inventoinnin- ja varastonhallinta > Kausittaiset tehtävät > Laadunhallinta > Laatutilaukset**.
2. Valitse [Tarkista tavaroiden laatu](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md) -ohjeessa luotu laatutilaus listasta.  

## <a name="create-a-nonconformance"></a>Luo määrityksistä poikkeaminen
1. Valitse toimintoruudussa **Kyselyt**.
2. Valitse **Määrityksistä poikkeamiset**.
3. Valitse **Uusi**.
4. Valitse **Ongelman tyyppi** -kentän avattavasta valikosta ongelma, joka löydettiin tarkastusprosessin aikana.  
5. Valitse **OK**.

## <a name="approvereject-a-nonconformance"></a>Hyväksy tai hylkää määrityksistä poikkeaminen
1. Valitse **Toiminnot**.
2. Valitse **Hyväksy määrityksistä poikkeaminen**. Hyväksy tässä esimerkissä määrityksistä poikkeamisen. Hyväksytyt määrityksistä poikkeamiset voidaan liittää liittyviin toimintoihin tallentamaan työ, joka tehdään osana määrityksistä poikkeamisen käsittelyä ja, kuten tässä ohjeaiheessa, korjauskäsittelyn käsittelyä.  
3. Valitse **Kyllä**.

## <a name="create-a-correction-action"></a>Luo korjaustoiminto
1. Valitse **Korjaukset**.
2. Valitse **Uusi**.
3. Valitse uuden rivin **Henkilöstönumero**-kentästä haluamasi tietue avattavasta valikosta.
4. Klikkaa **Valitse**.
5. Valitse **Liitä**. Luo korjausta koskeva huomautus. Tässä esimerkissä toimintona on yhteydenotto toimittajaan ja keskustelu määrityksistä poikkeamistapauksesta.  
6. Valitse **Uusi**.
7. Valitse **Muistiinpano**. Raporttiasetusten mukaan eri asiakirjatyyppejä voi tulostaa raportteihin, jotka liittyvät määrityksistä poikkeamisen hallintaan.  
8. Kirjoita **Kuvaus**-kenttään arvo.
9. Sulje sivu.

## <a name="maintain-a-correction"></a>Ylläpidä korjausta
1. Valitse **Merkitse valmiiksi**.
2. Valitse **OK**.
3. Sulje sivu.

## <a name="close-a-nonconformance"></a>Sulje määrityksistä poikkeaminen
1. Valitse **Toiminnot**.
2. Valitse **Sulje määrityksistä poikkeaminen**.
3. Valitse **Kyllä**.
4. Sulje sivut.
