---
title: Nimikkeen laaturyhmät
description: Tässä aiheessa kuvataan, kuinka ja luodaan nimikkeiden laaturyhmiä tuotteiden loogiseen ryhmittelemiseen siten, että ne voidaan liittää laatuliitoksiin laatutilausten automaattista luontia varten.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3074a6a8cc054be045bf593b509e76a1043af0b7
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956635"
---
# <a name="item-quality-groups"></a>Nimikkeen laaturyhmät

[!include [banner](../includes/banner.md)]

Laaturyhmän avulla voidaan määrittää nimikkeiden yhteisiä testausvaatimuksia. Tässä aiheessa kuvataan, kuinka ja luodaan nimikkeiden laaturyhmiä tuotteiden loogiseen ryhmittelemiseen siten, että ne voidaan liittää laatuliitoksiin laatutilausten automaattista luontia varten.

Voit määrittää, muokata ja tarkastella nimikkeitä, jotka on määritetty nimikkeelle määritettyihin laaturyhmiin, valitsemalla **Varastonhallinta \> Asetukset \> Laaturyhmät**. Kun olet määrittänyt testivaatimukset **Testiryhmät**-sivulla, voit määrittää laatutilausten automaattisen luonnin säännöt. Prosessin yksinkertaistamiseksi sääntöjä ei määritetä yksittäisille nimikkeille. Sen sijaan **Laatuliitokset**-sivulla määritetään laaturyhmän säännöt.

## <a name="example-of-an-item-quality-group"></a>Esimerkki nimikkeen laaturyhmästä

Teollisuusyritys ostaa useita eri raaka-aineita, joilla on samat testausvaatimukset tulevaa tarkistusta varten. Siksi yritys määrittää ensin laaturyhmän ja sitten nimiketunnukset, jotka liittyvät kyseisen ryhmän raaka-aineisiin. Yritys ostaa myöhemmin uutta raaka-ainetta, jolla on samat testausvaatimukset. Yritys ei määritä uudelle raaka-aineelle uusia testausvaatimuksia vaan lisää uuden materiaalin nimiketunnuksen aiemmin luotuun laaturyhmään.

Sama yritys myös tuottaa nimikkeitä, joilla on samat tuotannon testausvaatimukset, sekä lähettää nimikkeitä, joilla on samat vaatimukset lähetystä edeltävien testien suorittamiseksi. Siksi yritys määrittää ensin kaksi laaturyhmää lisää ja sitten kumpaankin soveltuvat nimiketunnukset.

## <a name="create-a-quality-group"></a>Laaturyhmän luominen

Voit luoda laaturyhmän seuraavasti.

1. Valitse **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Laaturyhmät**.
1. Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**. Määritä sitten uudelle rivillä seuraavat kentät:

    - **Laaturyhmä** – Määritä laaturyhmän yksilöivä tunnus tai nimi.
    - **Kuvaus** – Anna laaturyhmän yksityiskohtainen kuvaus.

1. Sulje sivu.

## <a name="manually-add-items-to-a-quality-group"></a>Lisää nimikkeet laaturyhmään manuaalisesti

Voit lisätä laaturyhmään nimikkeitä manuaalisesti noudattamalla seuraavia ohjeita.

1. Valitse **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Laaturyhmät**.
1. Valitse laaturyhmä, johon haluat lisätä nimikkeitä.
1. Valitse toimintoruudussa **Nimikkeet**.
1. Valitse **Laaturyhmän nimikkeet** -sivulla toimintoruudussa **Uusi** lisätäksesi rivin ruudukkoon. Määritä sitten uudelle riville **Nimiketunnus**-kentän arvoksi lisättävä nimiketunnus.
1. Toista edellinen vaihe kullekin lisättävälle nimikkeelle.
1. Sulje sivut.

## <a name="add-multiple-items-to-a-quality-group"></a>Lisää useita nimikkeitä laaturyhmään

Voit lisätä laaturyhmään useita nimikkeitä noudattamalla seuraavia ohjeita.

1. Valitse **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Laaturyhmät**.
1. Luo tai valitse laaturyhmä, johon haluat lisätä nimikkeitä.
1. Valitse toimintoruudussa **Lisää nimikkeitä**.
1. Anna lisättävien nimikkeiden suodatusehdot **Kysely**-valintaikkunaan. Voit esimerkiksi suodattaa tietyn nimikeryhmän kaikki nimikkeet.
1. Valitse **OK**.
1. **Lisää nimikkeitä** -valintaikkunassa ruudukko näyttää kaikki kyselyä vastaavat nimikkeet. Tarkastele tuloksia.

    Jos muutoksia tarvitaan, valitse **Valitse** palataksesi **Kysely**-valintaikkunaan ja muokkaa kyselyä.

1. Kun tulokset sisältävät kaikki lisättävät nimikkeet, valitse **OK**.
1. Sulje sivu.

## <a name="manually-associate-an-item-with-a-quality-group"></a>Nimikkeen liittäminen laaturyhmään manuaalisesti

Voit liittää laaturyhmään nimikkeen manuaalisesti noudattamalla seuraavia ohjeita.

1. Valitse **Varastonhallinta \> Asetukset \> Laadunvalvonta \> Nimikkeen laaturyhmät**.
1. Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Uusi**. Määritä sitten uudelle rivillä seuraavat kentät:

    - **Nimiketunnus** – Valitse lisättävä nimiketunnus.
    - **Laaturyhmä** – Valitse nimikkeeseen määritettävä laaturyhmä.

1. Toista edellinen vaihe kullekin nimikkeen lisäyhdistelmälle ja lisättävälle laaturyhmälle.
1. Sulje sivut.

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a>Laaturyhmän lisääminen manuaalisesti Vapautetut tuotteet -sivulta

Laaturyhmän lisäämiseksi manuaalisesti **Vapautetut tuotteet** -sivulta noudata näitä vaiheita.

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Valitse tuote, johon haluat liittää laaturyhmän.
1. Valitse toimintoruudun **Varastonhallinta**-välilehden **Laatu**-ryhmässä **Nimikkeen laaturyhmät**.
1. Valitse **Laaturyhmän nimikkeet** -sivulla toimintoruudussa **Uusi** lisätäksesi rivin ruudukkoon. Määritä sitten uudelle riville **Laaturyhmä**-kentän arvoksi laaturyhmä, jonka haluat määrittää tuotteeseen.
1. Toista edellinen vaihe kunkin tuotteeseen määritettävän laaturyhmän osalta.
1. Sulje sivut.

## <a name="additional-resources"></a>Lisäresurssit

- [Laadunhallinnan testin mittavälineet](quality-test-instruments.md)
- [Laadunhallinnan testit](quality-tests.md)
- [Laadunhallinnan testiryhmät](quality-test-groups.md)
- [Laadunhallinnan testimuuttujat](quality-test-variables.md)
- [Laatuliitokset](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
