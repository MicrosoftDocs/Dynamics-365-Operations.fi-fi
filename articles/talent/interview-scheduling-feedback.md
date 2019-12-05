---
title: Hakijoiden haastattelujen ajoittaminen Attractissa
description: Tässä ohjeaiheessa on tietoja haastattelujen aikataulutus- ja palautetehtävistä Attractissa.
author: hasrivas
manager: AnnBe
ms.date: 04/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: shielas
ms.openlocfilehash: 33eba9796ca997fde4be9a46050207d313551bde
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832742"
---
# <a name="schedule-interviews-in-attract"></a>Hakijoiden haastattelujen ajoittaminen Attractissa

[!include [banner](includes/banner.md)]

## <a name="scheduler-activity"></a>Ajastustehtävä

Valinnaisessa ajastustehtävässä on kaksi osaa: ehdokkaan käytettävyystietojen pyytäminen ja aikataulu. Ehdokkaan käytettävyystiedot -osassa voit pyytää ehdokkaan käytettävyystietoja sähköpostitse. Aikataulu-osassa voi sopia haastattelun ajankohdan ehdokkaan ja työhönottoryhmän kesken.

Määritä ajoitustehtävä sisältämään tai rajoittamaan ajoitettavia hakijoita valitsemalla arvo **Ketkä ajoitetaan** -kentässä. Käytettävissä ovat seuraavat vaihtoehdot: **Kaikki ehdokkaat**, **Ulkoiset ehdokkaat** ja **Sisäiset ehdokkaat**. Esimerkiksi, jos haluat ohittaa sisäiset ehdokkaat ajoituksen ensimmäisellä kierroksella, voit määrittää ajoitustoiminnon vain ulkoisille ehdokkaille määrittämällä **Ketkä ajoitetaan** -kentän arvoksi **Ulkoiset ehdokkaat**.

### <a name="candidate-availability-request"></a>Ehdokkaan käytettävyystietojen pyytäminen

Jos haluat pyytää ehdokkaiden käytettävyystietoja sähköpostitse, valitse **Pyydä ehdokkaan käytettävyystietoja** -kenttä. Jos kenttää ei valita, tätä vaihetta ei näytetä työn työhönottoprosessissa.

Voit pyytää käytettävyystietoja valitsemalla ensin **Lähetä pyyntö** ja sitten käytettävissä olevat päivämäärät ja sähköpostimallin. Lähetä sähköposti tämän jälkeen ehdokkaalle.

[![Attractin työhönottajan näkymä ehdokkaan käytettävyystietojen pyytämiseen](./media/scheduler-candidate-request.png)](./media/scheduler-candidate-request.png)

Kun ehdokas saa sähköpostiviestin, jossa häntä pyydetään vastaamaan pyyntöön, hän voi kirjautua ehdokasportaaliin, valita ensin hänelle sopivat päivämäärät ja valitse sitten **Lähetä**.

### <a name="schedule"></a>Aikataulu
Haastattelun ajastuksessa on useita määrityksiä, joiden avulla haastattelijoille ja ehdokkaalle lähetettävä haastatteluryhmä voidaan luoda.

1. Valitse **Luo aikataulu** ja lisää sitten **Lisää haastattelijoita** -ruudussa luetteloon kaikki haastattelijat, jotka tulevat haastatteluryhmään.
[![Attractin työhönottajanäkymän haastatteluryhmän ajoittamisen aloittamisesta](./media/schedule-start-over.png)](./media/schedule-start-over.png)   
    Jos ehdokas on vastannut haastattelun käytettävyystietopyyntöön, heidän valintansa on valmiina **Haastattelupvm**-kentässä. Voit valita tarvittaessa toisen päivämäärän.
    
    Jos valitset **Tee tästä paneelihaastattelu** -kentän, haastattelu luodaan siirtämällä vasemmalla oleva haastattelijaryhmä yhteen paneeliryhmään. Seuraavaksi on määritettävä haastattelujärjestys.
    
    Haastatteluaikataulu on järjestettävä siten, että se vastaa parhaiten osallistujien käytettävyystietoja. Jos kyse on sisäisestä hakijasta, voit sisällyttää heidän käytettävyystietonsa osaksi aikataulusuositusta.
    
    Jos haluat järjestää verkkotapaamisen, valitse **Lisää Skype-tapaamisia** -kenttä, jonka jälkeen jokaisessa haastattelutapahtumassa on **Skype for Business** -linkki.

2. Valitse kunkin haastattelutapahtuman kesto ja aloita sitten aikataulun luonti valitsemalla **OK**.

    Jos **Suositukset** on valittu, näkyviin tulee ehdotuksia ja haastatteluruudukko on täytetty valmiiksi. Näkyviin tulee kalenteri, jossa näkyy kaikkien valittujen haastattelijoiden käytettävyystiedot. Voit tarkastella myös sisäisen ehdokkaan kalenteria. Haastattelijoille ja sisäisille hakijoille voit tarkastella niiden varattuja ajankohtia, työaikoja, niiden poissaoloaikoja sekä määrittää myös, jos ne ovat merkinneet työskentelevänsä tietyn ajankohdan muualla. 

3. Jos ehdotuksia ei ole, napsauta **Haastattelijat**-sarakkeessa ajankohtaa, lisää haastattelun otsikko ja tiedot sekä täytä tarvittaessa sijaintitiedot. Voit halutessasi sisällyttää haastattelun **Skype for Business** -linkin.

4. Voit lisätä muita haastattelijoita valitsemalla haastattelijoita napsauttamalla **Lisää haastattelu** -ruudukon saraketta. Voit poistaa haastattelun ryhmästä kolme pistettä (...) -asetuksella.
    
5. Jos haastattelut on aikataulutettu ei aikavyöhykkeelle, valitse sopiva kaupunki/aikavyöhyke avattavasta luettelosta oikeassa yläkulmassa. Haastattelijan käytettävyysruudukko päivitetään vastaamaan uutta aikavyöhykettä. Tämä aikavyöhykevalinta näkyy nyt myös **Haastattelun yhteenveto** -näkymässä, joka jaetaan haastattelijoiden ja ehdokkaan kanssa. 

6. Lähetä kokouskutsut asianomaisille haastattelijoille valitsemalla **Lähetä haastattelijoille**.

    Sen jälkeen kun haastattelupyynnöt on lähetetty haastattelijoille, he voivat vastata suoraan heille lähetetystä sähköpostikutsusta.

    >[!NOTE]
    > Kaikkien yksilöhaastattelujen muistutukset lähetetään haastattelijoille 24 tunnin välein, jos haastattelija ei vastaa (hyväksyy tai hylkää) haastattelupyyntöön.

    > Paneelihaastatteluilla ei ole automaattisia muistutuksia haastattelupyynnöstä. Voit käynnistää muistutuksen manuaalisesti muokkaamalla haastattelua ja lähettämällä pyynnön takaisin haastattelijoille **Päivitä ja lähetä** -asetuksella.

    Haastattelijan vastaukset taltioidaan ja näytetään Attractissa. Jos haastattelija hylkää kutsun, sinua pyydetään tekemään muutos. Voit tarkastella vastausta **Ajoitus**-ruudukkonäkymässä puhekuplakuvaketta napsauttamalla.

[![Attractin työhönottaja näkymä haastattelijan vastauksesta](./media/schedule-interviewer-response2.png)](./media/schedule-interviewer-response2.png)

7. Kun haastatteluaikataulu on valmis ehdokkaan kanssa jaettavaksi, valitse **Lähetä ehdokkaalle**. Voit valita, piilotetaanko vai näytetäänkö haastattelijoiden nimet ja ajat ehdokkaalle.

8. Valitse sähköpostimalli ja lähetä haastattelun yhteenveto ehdokkaalle. Ehdokas voi tarkastella näitä tietoja sekä sähköpostissa että ehdokasportaalissa.
    
>[!NOTE] 
> Käytettävyystiedot näytetään ehdokkaan kalenterissa vain, jos kyse on sisäisestä ehdokkaasta. Samalla tavoin vain sisäisen ehdokkaan tietoja voidaan käyttää haastattelun aikataulusuosituksissa. Tällä hetkellä ehdokkaat (sisäiset tai ulkoiset) eivät saa kokouskutsua sähköpostitse, vaan ehdokas saa vain haastattelujen yhteenvedon.

Ehdokkaat saavat sähköpostiviestin, jossa on yhteenveto haastatteluryhmästä. Sähköpostiviestit sisältävät .ics-tiedoston, joka helpottaa käyttöä ja ilmoituksia haastattelun suhteen tallentamalla sen ehdokkaan omaan kalenteriin.

>[!TIP] 
> Jos lähetät haastatteluaikataulun hakijalle uudelleen, he saavat toisen .ics-liitetiedoston. On suositeltavaa päivittää hakijan haastatteluyhteenvedon sähköpostimallit, jotta varmistetaan, että ehdokkaat poistavat aiemmin lisätyt haastattelutapahtumat eivätkä näe kalenteritapahtumien kaksoiskappaleita. 

## <a name="feedback-activity"></a>Palautetehtävä

Palautetehtävä on työmallissa valinnainen. Tämän tehtävän avulla haastatteluun osallistuvat voivat antaa hakijaa koskevia suosituksia tai palautekommentteja. 

Voit sisällyttää tai rajoittaa hakijoita, joille voidaan antaa palautetta valitsemalla arvon **Kenelle haastattelijoiden tulisi antaa palautetta** -kentässä.  Käytettävissä ovat seuraavat vaihtoehdot: **Kaikki ehdokkaat**, **Ulkoiset ehdokkaat** ja **Sisäiset ehdokkaat**. Jos haluat esimerkiksi ohittaa sisäiset ehdokkaat ajoituksen ensimmäisellä kierroksella, määritä **Kenelle haastattelijoiden tulisi antaa palautetta** -kentän arvoksi **Ulkoiset ehdokkaat**.

Jos **Peri palautteeseen osallistujat työhönottoryhmältä** -kenttä valitaan, työnottaja, työhön ottava esimies ja haastattelijat siirtyvät automaattisesti palautetehtävään. Organisaatiot voit antaa haastattelijoille mahdollisuuden tarkastella muiden palautteet, ennen kuin he lähettävät oman palautteensa. Organisaatiot voivat lisäksi antaa haastattelijoille mahdollisuuden muokata jo lähetettyä palautetta. Haastattelijoita muistutetaan heidän äskettäin suorittamiensa haastattelujen palautteen lähettämisestä. Tämä muistutus perustuu työmallin osana tehtyihin valmiisiin määrityksiin. Työn työhön ottava esimies tai työhönottaja voivat halutessaan muistuttaa haastattelijaa palautteen lähettämisestä myös manuaalisesti.

## <a name="interview-activity"></a>Haastattelu-tehtävä

Valinnaisessa haastattelutehtävässä on kolme osaa: **ehdokkaan käytettävyystietojen pyytäminen**, **aikataulu** ja **palaute**. Käytä työmallin haastattelutehtävää, jos haluat kaikki ehdokkaan käytettävyystietojen pyytämiset aikataulun ja palautteen prosessin osaksi sen sijaan, että käyttäisit niitä yksittäin.

Voit sisällyttää tai rajoittaa haastateltavia ehdokkaita valitsemalla arvon **Ketä haastattelet** -kentässä. Käytettävissä ovat seuraavat vaihtoehdot: **Kaikki ehdokkaat**, **Ulkoiset ehdokkaat** ja **Sisäiset ehdokkaat**. Jos haluat esimerkiksi ohittaa sisäiset ehdokkaat haastatteluiden ensimmäisellä kierroksella, määritä **Ketä haastattelet** -kentän arvoksi **Ulkoiset ehdokkaat**.
