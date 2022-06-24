---
title: Muiden osavaltioiden toimittajien tuotteiden ICMS-DIF-verolaskelmien muutoksen perusta
description: Tässä artikkelin kuvataan ICMS-DIF-verotyypin laskelmien konfiguraatio, kun veroasiakirja vastaanotetaan Brasilian Rio Grande do Sulin (RS) tai São Paulon (SP) osavaltiossa.
author: Kai-Cloud
ms.date: 1/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-1-17
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 1fde18c79f375db4db6bc52cdb5c40a61625ae63
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868259"
---
# <a name="basis-change-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>Muiden osavaltioiden toimittajien tuotteiden ICMS-DIF-verolaskelmien muutoksen perusta

Tässä artikkelin kuvataan **ICMS-DIF**-verotyypin laskelmien konfiguraatio, kun veroasiakirja vastaanotetaan Brasilian Rio Grande do Sulin (RS) tai São Paulon (SP) osavaltiossa.

Valtion lain määritelmän mukaan kerätyn Imposto sobre Circulação de Mercadorias e Serviçosin (ICMS) on noudatettava tätä sääntöä:

*ICMS kerää* = ([(*Toiminnan määrä* – *ICMS lähteestä*) ÷ (1 – *ICMS % sisäinen*)] × *ICMS % sisäinen*) – *ICMS-määrä lähteestä*

## <a name="example"></a>Esimerkki

Brasilialainen RS-tilassa oleva yritys saa veroasiakirjan ostosta SP-tilassa olevalta toimittajalta. Yrityksen on kerättävä ICMS: n prosentuaalinen ero RS-valtion (18 prosenttia) ja SP-tilan (12 prosenttia) välillä. Pohja on kuitenkin laskettava edellisen säännön mukaisesti.

- **Operaation summa:** 1 000,00 Brasilian realia (1 000,00 R$)
- **ICMS osavaltioiden välinen:** 120,00 R$
- **ICMS-prosenttiosuus RS-tilassa:** 18 prosenttia
- **RS-tilassa kerättävä ICMS:** (\[(1 000 – 120) ÷ (1 – 0,18)\] × 0,18 ) – 120 = 73,17 R$ 

## <a name="resolution"></a>Ratkaisu

Jos haluat laskea differentiaali-ICMS:n (ICMS-DIF) RS-osavaltion sääntöjen mukaisesti, sinun on määritettävä arvonlisäverokoodit ja arvonlisäveroryhmä seuraavasti:

1. Luo arvonlisäverokoodi, joka vastaanottaa 12 prosentin ICMS:n (toisessa osavaltiossa). Tätä koodia käytetään rekisteröimään toimittajan verosaatavien summa.
2. Luo arvonlisäverokoodi ICMS-DIF:n keräämiseksi. Tämän arvonlisäverokoodin prosenttiosuuden on oltava 18 prosenttia (omassa valtiossasi), joka määrittää 18–12 prosentin eron. Määritä verotyypiksi **ICMS-DIF**. Tämä arvonlisäverokoodi on määritettävä laskentaparametreissa seuraavasti:

    - Valitse **Alkuperä**-kentässä **Bruttosumman prosenttiosuus**.
    - Valitse **Marginaaliperuste**-kentässä **Nettosumma riviä kohti** tai **Laskun saldon nettosumma**.
    - Määritä verotuskoodi siten, että sen verotuksellinen arvo on **3**. Tällä tavoin oikaisutapahtuma luodaan automaattisesti, kun **Verokirjat**-moduuli on käytössä.
    - Valitse arvonlisäveroryhmän konfiguraatiossa **ICMS-DIF**-arvonlisäverokoodin **Käyttövero**-vaihtoehto.
