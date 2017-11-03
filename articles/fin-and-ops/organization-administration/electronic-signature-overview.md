---
title: "Sähköisten allekirjoitusten yleiskuvaus"
description: "Tässä artikkelissa on yleiskatsaus sähköisistä allekirjoituksista ja niiden käyttämisestä Microsoft Dynamics 365 for Finance and Operationsissa."
author: maertenm
manager: AnnBe
ms.date: 08/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 698b938e515ff4755c2f111279cda244577ac9f3
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="electronic-signature-overview"></a><span data-ttu-id="e0391-103">Sähköisten allekirjoitusten yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="e0391-103">Electronic signature overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e0391-104">Tässä artikkelissa on yleiskatsaus sähköisistä allekirjoituksista ja niiden käyttämisestä Microsoft Dynamics 365 for Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="e0391-104">This article provides an overview of electronic signatures and describes how they can be used in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<a name="what-is-an-electronic-signature"></a><span data-ttu-id="e0391-105">Mikä on sähköinen allekirjoitus?</span><span class="sxs-lookup"><span data-stu-id="e0391-105">What is an electronic signature?</span></span>
--------------------------------

<span data-ttu-id="e0391-106">Sähköisellä allekirjoituksella vahvistetaan uuden tietojenkäsittelyprosessin aloittavan tai prosessin hyväksynnän aloittavan henkilön henkilöllisyys.</span><span class="sxs-lookup"><span data-stu-id="e0391-106">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="e0391-107">Joillakin aloilla sähköinen allekirjoitus on juridisesti yhtä sitova kuin käsin kirjoitettu.</span><span class="sxs-lookup"><span data-stu-id="e0391-107">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span> 

<span data-ttu-id="e0391-108">Sähköiset allekirjoitukset ovat pakollisia useilla säännöin ja määräyksin säädellyillä aloilla, kuten lääketeollisuudessa, elintarviketeollisuudessa sekä ilmailu- ja maanpuolustusteollisuudessa.</span><span class="sxs-lookup"><span data-stu-id="e0391-108">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span> <span data-ttu-id="e0391-109">Niiden käyttämistä edellyttää myös Yhdysvaltain elintarvike- ja lääkeviranomaisen (FDA) määräys 21 CFR Part 11.</span><span class="sxs-lookup"><span data-stu-id="e0391-109">They are also required for compliance with regulations in 21 CFR Part 11 that was issued by the Food and Drug Administration (FDA) in the United States.</span></span> 

<span data-ttu-id="e0391-110">**Huomautus:** Sähköinen allekirjoitus ei ole sama kuin digitaalinen allekirjoitus.</span><span class="sxs-lookup"><span data-stu-id="e0391-110">**Note:** An electronic signature by itself isn't the same as a digital signature.</span></span> <span data-ttu-id="e0391-111">Sähköinen allekirjoitus on yksinkertaisesti käsin kirjoitetun allekirjoituksen korvike, kun taas digitaalinen allekirjoitus sisältää lisäsuojaustoimenpiteitä.</span><span class="sxs-lookup"><span data-stu-id="e0391-111">An electronic signature is just a substitute for a handwritten signature, whereas a digital signature provides additional security measures.</span></span> <span data-ttu-id="e0391-112">Digitaalisen allekirjoituksen avulla voi tunnistaa, onko toinen käyttäjä tai prosessi peukaloinut tietoja.</span><span class="sxs-lookup"><span data-stu-id="e0391-112">A digital signature can help identify whether another user or process has tampered with the data.</span></span> <span data-ttu-id="e0391-113">Digitaalisen allekirjoituksen voi myös vahvistaa, eikä tietojen allekirjoittamiseen käytetyn sertifikaatin omistaja voi kumota tätä vahvistusta.</span><span class="sxs-lookup"><span data-stu-id="e0391-113">A digital signature can also be verified, and this verification can't be refuted by the owner of the certificate that was used to sign the data.</span></span> <span data-ttu-id="e0391-114">Kuten alla on kuvattu, Microsoft Dynamics 365 for Finance and Operationsin sähköisissä allekirjoituksissa on sisäinen digitaalisten allekirjoitusten toiminto.</span><span class="sxs-lookup"><span data-stu-id="e0391-114">As described below, electronic signatures in Microsoft Dynamics 365 for Finance and Operations have built-in digital signature functionality.</span></span>

## <a name="electronic-signatures-in-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="e0391-115">Microsoft 365 for Finance and Operationsin sähköiset allekirjoitukset</span><span class="sxs-lookup"><span data-stu-id="e0391-115">Electronic signatures in Dynamics 365 for Finance and Operations</span></span>
<span data-ttu-id="e0391-116">Voit käyttää Finance and Operationsissa sähköisiä allekirjoituksia tärkeissä liiketoimintaprosesseissa.</span><span class="sxs-lookup"><span data-stu-id="e0391-116">In Finance and Operations, you can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="e0391-117">Joissakin prosesseissa on sisäinen sähköisten allekirjoitusten toiminto.</span><span class="sxs-lookup"><span data-stu-id="e0391-117">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="e0391-118">Voit myös luoda mukautettuja allekirjoitusvaatimuksia mille tahansa tietokannan taululle ja kentälle.</span><span class="sxs-lookup"><span data-stu-id="e0391-118">You can also create custom signature requirements for any database table and field.</span></span> 

<span data-ttu-id="e0391-119">Sähköisissä allekirjoituksissa on sisäinen digitaalisten allekirjoitusten toiminto.</span><span class="sxs-lookup"><span data-stu-id="e0391-119">Electronic signatures have built-in digital signature functionality.</span></span> <span data-ttu-id="e0391-120">Jokaisen tiedostoja allekirjoittavan käyttäjän on hankittava voimassa oleva salaussertifikaatti.</span><span class="sxs-lookup"><span data-stu-id="e0391-120">Every user who signs documents must obtain a valid cryptographic certificate.</span></span> <span data-ttu-id="e0391-121">Kun tiedosto allekirjoitetaan, tähän sertifikaattiin liittyvä yksityinen avain vahvistetaan.</span><span class="sxs-lookup"><span data-stu-id="e0391-121">When a document is signed, the private key that is associated with that certificate is validated.</span></span> <span data-ttu-id="e0391-122">Finance and Operations kirjaa sähköisten allekirjoitusten tiedot lokiin kirjausketjua varten.</span><span class="sxs-lookup"><span data-stu-id="e0391-122">Finance and Operations records electronic signature information in a log to provide an audit trail.</span></span> <span data-ttu-id="e0391-123">Lisätietoja sähköisistä allekirjoituksista on artikkelissa [Määritä sähköiset allekirjoitukset (ohjattu tehtävä)](tasks/set-up-electronic-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="e0391-123">To set up electronic signatures, see [Set up electronic signatures (Task guide)](tasks/set-up-electronic-signatures.md).</span></span>

## <a name="users-who-require-access-to-electronic-signatures"></a><span data-ttu-id="e0391-124">Käyttäjät, joiden on voitava käyttää sähköisiä allekirjoituksia</span><span class="sxs-lookup"><span data-stu-id="e0391-124">Users who require access to electronic signatures</span></span>
<span data-ttu-id="e0391-125">Kolmenlaiset käyttäjät tarvitsevat tavallisesti pääsyn sähköisiin allekirjoituksiin: sähköisten allekirjoitusten järjestelmänvalvojat, allekirjoittajat ja sähköisten allekirjoitusten tarkastajat.</span><span class="sxs-lookup"><span data-stu-id="e0391-125">Three kinds of users typically require security access to electronic signatures: electronic signature administrators, signers, and electronic signature auditors.</span></span>

### <a name="electronic-signature-administrator"></a><span data-ttu-id="e0391-126">Sähköisten allekirjoitusten järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="e0391-126">Electronic signature administrator</span></span>

<span data-ttu-id="e0391-127">Sähköisten allekirjoitusten järjestelmänvalvoja määrittää allekirjoitusvaatimukset, yleisparametrit ja hyväksyjät sekä saa hälytyksiä, kun allekirjoituksia ei voida vahvistaa.</span><span class="sxs-lookup"><span data-stu-id="e0391-127">The electronic signature administrator sets up signature requirements, general parameters, and approvers, and receives alerts when signatures can't be verified.</span></span> <span data-ttu-id="e0391-128">Oletusarvon mukaan **Tietotekniikkapäällikkö**-käyttöoikeusrooliin kuuluvalla käyttäjällä on sähköisten allekirjoitusten hallintaoikeudet.</span><span class="sxs-lookup"><span data-stu-id="e0391-128">By default, a user who belongs to the **Information technology manager** security role has permission to administer electronic signatures.</span></span>

### <a name="signer"></a><span data-ttu-id="e0391-129">Allekirjoittaja</span><span class="sxs-lookup"><span data-stu-id="e0391-129">Signer</span></span>

<span data-ttu-id="e0391-130">Allekirjoittaja antaa sähköisiä allekirjoituksia tiedostoihin ja prosesseihin, joissa allekirjoituksia vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="e0391-130">A signer provides electronic signatures for documents and processes that require signatures.</span></span> <span data-ttu-id="e0391-131">Oletusarvon mukaan **Järjestelmän käyttäjä** -käyttöoikeusrooliin kuuluvalla käyttäjällä on oikeus allekirjoittaa asiakirjoja sähköisesti.</span><span class="sxs-lookup"><span data-stu-id="e0391-131">By default, a user who belongs to the **System user** security role has permission to sign documents electronically.</span></span> 

<span data-ttu-id="e0391-132">**Huomautus:** Allekirjoittaja saattaa tarvita lisäkäyttöoikeuksia, ennen kuin hänelle myönnetään allekirjoitettavaan tiedoston tai prosessiin liittyvien tietojen käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="e0391-132">**Note:** The signer might require additional permissions before access is granted to data that is related to the document or process that is being signed.</span></span> <span data-ttu-id="e0391-133">Käyttäjällä, joka tekee muutoksia tietoihin ja jonka on sitten allekirjoitettava nämä muutokset, on oltava oikeus muuttaa tietoja.</span><span class="sxs-lookup"><span data-stu-id="e0391-133">A user who changes data and must then sign for those changes must have permission to change the data.</span></span> <span data-ttu-id="e0391-134">Käyttäjä, joka allekirjoittaa toisen käyttäjän puolesta, ei ehkä tarvitse pääsyä tietoihin.</span><span class="sxs-lookup"><span data-stu-id="e0391-134">A user who signs on behalf of another user might not require access to the data.</span></span> <span data-ttu-id="e0391-135">Esimerkki tällaisesta käyttäjästä on esimies, joka allekirjoittaa työntekijän muutokset.</span><span class="sxs-lookup"><span data-stu-id="e0391-135">An example of this kind of user is a supervisor who signs for an employee's changes.</span></span>

### <a name="electronic-signature-auditor"></a><span data-ttu-id="e0391-136">Sähköisten allekirjoitusten tarkastaja</span><span class="sxs-lookup"><span data-stu-id="e0391-136">Electronic signature auditor</span></span>

<span data-ttu-id="e0391-137">Sähköisten allekirjoitusten tarkastaja tarkistaa tietokantalokin sekä allekirjoituksen tarkistuslokin, jota voi käyttää tietokantalokista.</span><span class="sxs-lookup"><span data-stu-id="e0391-137">The electronic signature auditor reviews the database log and the signature review log that is available from the database log.</span></span> <span data-ttu-id="e0391-138">Oletusarvon mukaan **Tietotekniikkapäällikkö**-käyttöoikeusrooliin kuuluvalla käyttäjällä on sähköisten allekirjoitusten tarkistusoikeudet.</span><span class="sxs-lookup"><span data-stu-id="e0391-138">By default, a user who belongs to the **Information technology manager** security role has permission to audit electronic signatures.</span></span> 

<span data-ttu-id="e0391-139">Jos käytät muuta kuin **Tietotekniikkapäällikkö**-roolia, varmista, että roolille on määritelty seuraavat oikeudet:</span><span class="sxs-lookup"><span data-stu-id="e0391-139">If you use a role other than **Information technology manager**, make sure that the role is assigned the following privileges:</span></span>

-   <span data-ttu-id="e0391-140">Tarkastele sähköisen allekirjoituksen virheitä</span><span class="sxs-lookup"><span data-stu-id="e0391-140">View electronic signature failures</span></span>
-   <span data-ttu-id="e0391-141">Tarkastele tietokantalokia</span><span class="sxs-lookup"><span data-stu-id="e0391-141">View database log</span></span>

## <a name="signing-documents-electronically"></a><span data-ttu-id="e0391-142">Asiakirjojen allekirjoittaminen sähköisesti</span><span class="sxs-lookup"><span data-stu-id="e0391-142">Signing documents electronically</span></span>
### <a name="get-a-certificate"></a><span data-ttu-id="e0391-143">Sertifikaatin hakeminen</span><span class="sxs-lookup"><span data-stu-id="e0391-143">Get a certificate</span></span>

<span data-ttu-id="e0391-144">Sinun on pyydettävä sertifikaatti ennen tiedostojen sähköistä allekirjoitusta Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="e0391-144">Before you sign documents electronically in Finance and Operations, you must request a certificate.</span></span> 

<span data-ttu-id="e0391-145">**Huomautus:** Finance and Operations käyttää Microsoft SQL Serverin ominaisuuksia sertifikaattien luomiseen ja sähköisten allekirjoitusten käyttöönottoon.</span><span class="sxs-lookup"><span data-stu-id="e0391-145">**Note:** Finance and Operations uses Microsoft SQL Server features to create certificates and enable electronic signing.</span></span> <span data-ttu-id="e0391-146">Muuta sertifikaattia tai julkisen avaimen infrastruktuuria ei tarvita.</span><span class="sxs-lookup"><span data-stu-id="e0391-146">No additional certificate or public key infrastructure (PKI) is required.</span></span> 

<span data-ttu-id="e0391-147">Kun pyydät sertifikaattia, sinulle luodaan julkinen avain ja yksityinen avain Finance and Operations -tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="e0391-147">When you request a certificate, a public key and a private key are created for you in the Finance and Operations database.</span></span> <span data-ttu-id="e0391-148">Yksityinen avain salataan vain sinun tuntemallasi salasanalla.</span><span class="sxs-lookup"><span data-stu-id="e0391-148">The private key is encrypted by using a password that is known only to you.</span></span> <span data-ttu-id="e0391-149">Kun allekirjoitat tiedoston sähköisesti, henkilöllisyytesi tarkistetaan kirjoittaessasi salasanan.</span><span class="sxs-lookup"><span data-stu-id="e0391-149">When you sign a document electronically, your identity is verified when you enter the password.</span></span> 

<span data-ttu-id="e0391-150">Pyydä sertifikaatti valitsemalla **Asetukset**-sivun **Tilit**-välilehdessä **Hanki sertifikaatti**.</span><span class="sxs-lookup"><span data-stu-id="e0391-150">To request a certificate, on the **Options** page, on the **Accounts** tab, click **Get certificate**.</span></span> 

<span data-ttu-id="e0391-151">Kirjoita ja vahvista salasana, jota käytät allekirjoittamiseen.</span><span class="sxs-lookup"><span data-stu-id="e0391-151">You must enter and confirm the password that you will use for signing.</span></span> <span data-ttu-id="e0391-152">Salasanalla suojataan yksityistä avaintasi ja hyväksytään sertifikaattisi käyttö.</span><span class="sxs-lookup"><span data-stu-id="e0391-152">The password is used to protect your private key and authorize the use of your certificate.</span></span> <span data-ttu-id="e0391-153">Tätä salasanaa ei tallenneta tietokantaan eikä se ole kenenkään muun käytettävissä – ei edes Finance and Operations -järjestelmänvalvojan käytössä.</span><span class="sxs-lookup"><span data-stu-id="e0391-153">This password isn't stored in the database, and it isn't available to anyone else, not even to the Finance and Operations administrator.</span></span> 

<span data-ttu-id="e0391-154">Jos unohdat sertifikaattiisi liittyvän salasanan, sertifikaatti on vaihdettava.</span><span class="sxs-lookup"><span data-stu-id="e0391-154">If you forget the password that is connected with your certificate, that certificate must be reset.</span></span> <span data-ttu-id="e0391-155">Jos vaihdat sertifikaatin, se ei vaikuta aiemmalla sertifikaatilla allekirjoitettuihin asiakirjoihin.</span><span class="sxs-lookup"><span data-stu-id="e0391-155">If you reset the certificate, you don't affect documents that you signed by using the previous certificate.</span></span> <span data-ttu-id="e0391-156">Voit vaihtaa sertifikaatin valitsemalla **Asetukset** -sivulla **Palauta sertifikaatti**.</span><span class="sxs-lookup"><span data-stu-id="e0391-156">To reset the certificate, on the **Options** page, click **Reset certificate**.</span></span>

### <a name="sign-a-document-electronically"></a><span data-ttu-id="e0391-157">Asiakirjan allekirjoittaminen sähköisesti</span><span class="sxs-lookup"><span data-stu-id="e0391-157">Sign a document electronically</span></span>

<span data-ttu-id="e0391-158">**Allekirjoita tiedosto** -sivu avautuu, kun teet sähköistä allekirjoitusta edellyttävän muutoksen.</span><span class="sxs-lookup"><span data-stu-id="e0391-158">The **Sign document** page is displayed when you make a change that requires an electronic signature.</span></span>

1.  <span data-ttu-id="e0391-159">Tarkista tiedoston muutokset valitsemalla **Allekirjoita tiedosto** -sivulla **Tiedosto**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="e0391-159">On the **Sign document** page, click the **Document** tab to review the changes to the document.</span></span>
2.  <span data-ttu-id="e0391-160">Valitse syykoodi **Allekirjoitus**-välilehdestä.</span><span class="sxs-lookup"><span data-stu-id="e0391-160">On the **Signature** tab, select a reason code.</span></span>
3.  <span data-ttu-id="e0391-161">Kirjoita kommentti, jos se on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="e0391-161">Enter a comment, if a comment is required.</span></span>
4.  <span data-ttu-id="e0391-162">Jos käyttäjätunnuksesi ei näy **Allekirjoittaja**-kentässä, valitse se luettelossa.</span><span class="sxs-lookup"><span data-stu-id="e0391-162">If your user ID doesn't appear in the **Signer** field, select it in the list.</span></span>
5.  <span data-ttu-id="e0391-163">Anna sijaintisi, jos tämä tieto on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="e0391-163">Enter your location, if this information is required.</span></span>
6.  <span data-ttu-id="e0391-164">Napsauta **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0391-164">Click **OK**.</span></span>

### <a name="sign-for-another-users-changes"></a><span data-ttu-id="e0391-165">Kirjaa toisen käyttäjän muutokset</span><span class="sxs-lookup"><span data-stu-id="e0391-165">Sign for another user's changes</span></span>

<span data-ttu-id="e0391-166">Joskus voi olla tarpeen, että käyttäjä allekirjoittaa toisen käyttäjän muutokset.</span><span class="sxs-lookup"><span data-stu-id="e0391-166">Occasionally, you might want a user to sign for another user's changes.</span></span> <span data-ttu-id="e0391-167">Esimerkiksi esimiehen on joskus allekirjoitettava työntekijän tuoterakenteeseen tekemät muutokset.</span><span class="sxs-lookup"><span data-stu-id="e0391-167">For example, a supervisor might be required to sign for changes that an employee makes to a bill of materials (BOM).</span></span> <span data-ttu-id="e0391-168">Tällä menetelmällä voit määrittää Finance and Operations -käyttäjän allekirjoittajaksi, joka tekee allekirjoitukset toisen käyttäjän puolesta.</span><span class="sxs-lookup"><span data-stu-id="e0391-168">Use this procedure to designate a Finance and Operations user as a signer for another user.</span></span> 

<span data-ttu-id="e0391-169">**Huomautukset:** Kun käyttäjä allekirjoittaa toisen käyttäjän muutoksen, allekirjoitus on tehtävä muutoksen tehneen käyttäjän työasemassa.</span><span class="sxs-lookup"><span data-stu-id="e0391-169">**Note:** When one user signs for another user's change, the signature must be provided at the workstation of the user who made the change.</span></span> <span data-ttu-id="e0391-170">Käyttäjä ei voi tallentaa muutosta, ennen kuin allekirjoitus on annettu.</span><span class="sxs-lookup"><span data-stu-id="e0391-170">The user can't save the change until the signature has been provided.</span></span> 

<span data-ttu-id="e0391-171">Määritä hyväksyjät seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="e0391-171">To designate approvers, follow these steps.</span></span>

1.  <span data-ttu-id="e0391-172">Valitse **Asetukset**-sivun **Tilit**-välilehdessä **Määritä hyväksyjä**.</span><span class="sxs-lookup"><span data-stu-id="e0391-172">On the **Options** page, on the **Accounts** tab, click **Designate approver**.</span></span>
2.  <span data-ttu-id="e0391-173">Valitse sen käyttäjän tunnus, jonka on allekirjoitettava toisen käyttäjän muutokset **Hyväksyjän käyttäjätunnus** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="e0391-173">In the **Approver user ID** field, select the ID of the user who must sign for another user's changes.</span></span>
3.  <span data-ttu-id="e0391-174">Valitse sen käyttäjän tunnus, jonka muutokset on allekirjoitettava **Käyttäjätunnus, jonka puolesta allekirjoitetaan** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="e0391-174">In the **Sign for user ID** field, select the ID of the user whose changes must be signed for.</span></span>





