---
title: Työajan seurannan poissaolojen rekisteröinti
description: Tässä ohjeaiheessa kerrotaan, miten poissaolojen rekisteröintejä käsitellään työajan seurannassa.
author: johanhoffmann
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JMGParameters, JmgAbsenceCalendar
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b765ae63cfb17e26439758f2a0ed64770ef70881
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809275"
---
# <a name="absence-registration-in-time-and-attendance"></a>Työajan seurannan poissaolojen rekisteröinti

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa esitellään poissaoloihin liittyvät käsitteet ja kerrotaan, miten poissaoloja käsitellään työajan seurannassa.

## <a name="absence-that-is-based-on-regular-work-hours"></a>Normaaleihin työtunteihin perustuva poissaolo

Kun työntekijät eivät työskentele normaalien työtuntien aikana, heille kirjataan poissaolo. Normaalit työtunnit määritetään työntekijän normaalin työajan profiilissa.

Tässä esimerkissä työntekijä työskentelee sellaisen päiväprofiilin mukaan, jossa sisäänleimaus tehdään kello 7.00 ja ulosleimaus kello 15.00. Jos työntekijä leimaa itsensä sisään kello 9.00, hänelle kirjataan kyseiseltä päivältä poissaolo ajalta 7.00–9.00.

Tässä tapauksessa työntekijöitä pyydetään antamaan poissaolon syy. He voivat määrittää syyn valitsemalla poissaolokoodin.

## <a name="absence-codes"></a>Poissaolokoodit

Poissaolokoodit määrittävät erilaiset poissaolon tyypit. Yritys määrittää poissaolokoodit.

Poissaolokoodeihin voi kohdistaa erilaisia sääntöjä. Poissaolokoodi voidaan määrittää esimerkiksi maksun palkan pienentämistä tai myöntämistä varten.

Tässä esimerkissä yritys määrittää **Myöhässä**-poissaolokoodin, jota työntekijät käyttävät saapuessaan töihin myöhässä ilman hyvää syytä. Yritys määrittää myös **Sisäinen kurssi** -poissaolokoodin, jota työntekijät käyttävät osallistuessaan sisäisille kursseille. Nämä poissaolokoodit voidaan määrittää niin, että **Myöhässä**-koodi pienentää työntekijän palkkaa, mutta **Sisäinen kurssi** -koodi ei.

Voit määrittää automaattisia poissaolokoodeja. Näitä poissaolokoodeja voi käyttää työntekijän työajan laskemisessa, kun poissaoloa ei ole rekisteröity. Työntekijän aikaprofiili määrittää, käytetäänkö normaalin työajan tai liukuma-ajan poissaolokoodia.

### <a name="set-up-standard-time-and-flex-time"></a>Normaalin työajan ja liukuma-ajan määrittäminen

- Määritä normaalin työajan ja liukuma-ajan parametrit käyttämällä **Automaattinen poissaolon lisäys**- ja **Automaattinen liukuvan työajan lisäys** -vaihtoehtoa **Työajan seurannan parametrit** -sivulla.

## <a name="absence-groups"></a>Poissaoloryhmät

Poissaolokoodit ryhmitellään poissaoloryhmiksi. Poissaoloryhmien avulla ryhmitellään poissaolokoodit, joilla on yhteisiä ominaisuuksia. Esimerkkejä ovat poissaolokoodit, joiden syy on luvallinen poissaolo tai esimerkiksi lääkärikäynti, valamiespalvelu tai sairas lapsi.

## <a name="planned-absence"></a>Suunniteltu poissaolo

Jos tiedetään, että työntekijä on poissa tietyn ajan, kuten esimerkiksi tulevan loman ajan, voidaan käyttää suunniteltua poissaoloa. Suunniteltu poissaolo määritetään poissaolokoodien avulla niin, että koodit ottavat huomioon suunnitellun poissaolon. Kun määrität suunnitellun poissaolon, sinulta ei pyydetä poissaolokoodia poissaolojakson aikana aikarekisteröintien laskemisen yhteydessä. Suunniteltu poissaolo voidaan määrittää yksittäiselle työntekijälle. Työntekijöiden suunnitellun poissaolon joukkopäivitystä varten voidaan myös määrittää erätyö.

### <a name="set-up-planned-absence"></a>Suunnitellun poissaolon määrittäminen

1. Valitse **Henkilöstöhallinto** &gt; **Työntekijät** &gt; **Työntekijät** ja valitse työntekijä.
2. Valitse **Aika** &gt; **Aikamääritykset** &gt; **Ajan poissaolomerkintä** ja määritä suunniteltu poissaolo.

## <a name="interrupted-planned-absence"></a>Keskeytetty suunniteltu poissaolo

Jos käytät **Keskeytys**-vaihtoehtoa suunnitellun poissaolon määrityksen yhteydessä, suunniteltu poissaolo keskeytetään, jos työntekijä kirjautuu sisään suunnitellun poissaolojakson aikana. Suunniteltu poissaolo merkitään **keskeytetyksi**. Poissaolo ei vaikuta tuleviin laskelmiin.

### <a name="set-up-a-planned-absence-for-interruption"></a>Suunnitellun poissaolon määrittäminen keskeytystä varten

1. Avaa **Ajan poissaolomerkintä** -sivu suunnitellun poissaolon määrittämisen yhteydessä kerrotulla tavalla.
2. Valitse **Keskeytä**.

**Keskeytä**-vaihtoehtoa käytetään, kun aika rekisteröidään työnohjauksen päätteessä tai laitteessa. Vaihtoehtoa ei käytetä, jos rekisteröinnit syötetään laskenta- ja hyväksyntäsivuilla tai **Sähköinen kellokortti** -sivulla.

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a>Esimerkkejä poissaolon käyttämisestä liukumaprofiilissa

Seuraavat kolme esimerkkiä näyttävät, miten poissaolo lasketaan profiilille, jolle on määritetty liukuvat jaksot.

Esimerkeissä käytetään seuraavaa profiilia.

| Saapuminen | Vakioaika    | Tauko             | Vakioaika | Vaje-        | Poistuminen | Ylijäämä        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| 8.00     | 9.00–11.30 | 11.30–12.00 | 12.00–15.00 | 15.00–16.00 | 16.00      | 16.00–18.00 |

### <a name="example-1-signing-out-during-a-flex--period"></a>Esimerkki 1: Kirjautuminen ulos liukuman vähennysjakson aikana

Työntekijä leimaa itsensä sisään kello 8.00 ja ulos kello 15.30. Koska työntekijä leimaa itsensä ulos liukuman vähennysjakson aikana, poissaoloa ei kirjata, vaan työntekijän liukumasaldosta vähennetään puoli tuntia.

### <a name="example-2-signing-out-in-during-standard-time-period"></a>Esimerkki 2: Kirjautuminen ulos normaalin työjakson aikana

Työntekijä leimaa itsensä sisään kello 8.00 ja ulos kello 14.30. Koska työntekijä leimaa itsensä ulos normaalin työjakson aikana, poissaoloksi lasketaan kello 14.30–16.00 välinen aika. Rekisteröity poissaolojakso on 1,5 tuntia. Jakson poissaolokoodi on annettava.

### <a name="example-3-signing-out-during-a-flex-period"></a>Esimerkki 3: Kirjautuminen ulos liukuman lisäysjakson aikana

Työntekijä leimaa itsensä sisään kello 8.00 ja ulos kello 16.30. Koska työntekijä leimaa itsensä ulos liukuman lisäysjakson aikana, poissaoloa ei kirjata, vaan työntekijän liukumasaldoon lisätään puoli tuntia.

## <a name="absence-in-the-calculation-and-approval-process"></a>Poissaolo laskennassa ja hyväksyntäprosessi

Työntekijän aikarekisteröinnit on laskettava ja hyväksyttävä, ennen kuin ne voidaan siirtää palkanlaskentajärjestelmän maksukohteiksi.

Hyväksyjä voi muuttaa työntekijän aikarekisteröintejä. Hyväksyjä voi muuttaa jopa mitä tahansa työntekijän rekisteröimää poissaoloa. Jos hyväksyjä syöttää poissaolokoodin sisältävän ajanjakson manuaalisesti, työajan seurannan parametrien oletuspoissaolokoodi ei korvaa kyseisen jakson poissaolokoodia.

Tässä esimerkissä työntekijä leimaa itsensä sisään kello 10.00 ja valitsee myöhästymisen osoittavan poissaolokoodin. Myöhemmin työntekijä ilmoittaa esimiehelle, että hänellä oli aika lääkärille kello 8.00–10.00. Lääkärissäkäynti ei aiheuta vähennystä työntekijän palkasta. Tämän vuoksi esimies voi tässä tapauksessa korjata kello 8.00 ja 10.00 väliset kaksi tuntia manuaalisesti syöttämällä poissaolokoodin, joka osoittaa näiden kahden tunnin poissaolon syyksi sairauden.

### <a name="calculate-and-approve-absence"></a>Poissaolon laskeminen ja hyväksyminen

- Valitse **Työajan seuranta** &gt; **Tarkista ja hyväksy** &gt; **Hyväksy tai laske**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]