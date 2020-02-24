---
title: การรับรองความถูกต้อง
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 025feca31eed8649bc319a1e1a1b6d1af3ddb128
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010780"
---
# <a name="authentication"></a><span data-ttu-id="f5628-102">การรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="f5628-102">Authentication</span></span>

<span data-ttu-id="f5628-103">บทความนี้แสดงข้อมูลภาพรวมเกี่ยวกับวิธีการรับรองความถูกต้องของข้อมูลอินเทอร์เฟสโปรแกรมประยุกต์ (API) ของ Microsoft Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="f5628-103">This article provides overview information about how to authenticate with the Microsoft Dynamics 365 Human Resources data application programming interface (API).</span></span>

## <a name="overview"></a><span data-ttu-id="f5628-104">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="f5628-104">Overview</span></span>

<span data-ttu-id="f5628-105">API ข้อมูลสำหรับทรัพยากรบุคคลเป็นการดำเนินการ OData</span><span class="sxs-lookup"><span data-stu-id="f5628-105">The data API for Human Resources is an OData implementation.</span></span> <span data-ttu-id="f5628-106">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [เปิดโพรโทคอลข้อมูล (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md)</span><span class="sxs-lookup"><span data-stu-id="f5628-106">For more information, see [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span></span>

<span data-ttu-id="f5628-107">ใบสมัครของคุณต้องรับรองความถูกต้องเป็นผู้เรียกที่ได้รับอนุญาตก่อนที่ API จะมีการร้องขอการบริการจากแอพลิเคชันของคุณ</span><span class="sxs-lookup"><span data-stu-id="f5628-107">Your application must authenticate as an authorized caller before the API will service requests from your application.</span></span>

## <a name="fundamentals"></a><span data-ttu-id="f5628-108">พื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="f5628-108">Fundamentals</span></span>

<span data-ttu-id="f5628-109">เมื่อต้องการเรียก API ข้อมูลแอพลิเคชันของคุณจะต้องได้รับการเข้าถึงจากแพลตฟอร์ม Microsoft identity</span><span class="sxs-lookup"><span data-stu-id="f5628-109">To call the data API, your application must acquire an access token from the Microsoft identity platform.</span></span> <span data-ttu-id="f5628-110">โทเคนการเข้าถึงประกอบด้วยข้อมูลเกี่ยวกับใบสมัครของคุณและสิทธิ์การได้รับอนุญาตที่มีการเรียกทรัพยากรในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="f5628-110">The access token contains information about your application and the permission that it has to call resources in Human Resources.</span></span>

### <a name="access-token"></a><span data-ttu-id="f5628-111">โทเคนการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="f5628-111">Access token</span></span>

<span data-ttu-id="f5628-112">โทเคนการเข้าถึงที่ออกโดยแพลตฟอร์มข้อมูลเฉพาะของ Microsoft คือ base64 –การเข้ารหัสเว็บโทเคนโทเคน (JWTs) ของ JavaScript Object Notation (JSON)</span><span class="sxs-lookup"><span data-stu-id="f5628-112">Access tokens issued by the Microsoft identity platform are base64–encoded JavaScript Object Notation (JSON) Web Tokens (JWTs).</span></span> <span data-ttu-id="f5628-113">มีข้อมูล (การอ้างสิทธิ์) ที่ API ข้อมูล (และเว็บ APIs อื่นๆที่มีการรักษาความปลอดภัยโดยแพลตฟอร์ม Microsoft identity) ใช้เพื่อตรวจสอบความถูกต้องของผู้เรียกและตรวจสอบให้แน่ใจว่าผู้เรียกมีสิทธิ์ที่ถูกต้องในการดำเนินการที่ผู้ใช้เหล่านั้นกำลังร้องขอ</span><span class="sxs-lookup"><span data-stu-id="f5628-113">They contain information (claims) that the data API (and other web APIs that are secured by the Microsoft identity platform) use to validate the caller and make sure that the caller has the correct permissions to perform the operation they're requesting.</span></span> <span data-ttu-id="f5628-114">ในระหว่างการเรียกคุณสามารถรักษาโทเคนการเข้าถึงเป็นแบบทึบ</span><span class="sxs-lookup"><span data-stu-id="f5628-114">During calls, you can treat access tokens as opaque.</span></span> <span data-ttu-id="f5628-115">คุณควรส่งโทเคนการเข้าถึงไปยังช่องทางที่ปลอดภัย เช่น ความปลอดภัยการขนส่งเลเยอร์ (TLS) และความปลอดภัยของโพรโทคอลการโอนถ่ายข้อมูลแบบ Hypertext (HTTPS) </span><span class="sxs-lookup"><span data-stu-id="f5628-115">You should always transmit access tokens over a secure channel, such as Transport Layer Security (TLS) and Hypertext Transfer Protocol Secure (HTTPS).</span></span>

<span data-ttu-id="f5628-116">ต่อไปนี้เป็นตัวอย่างของโทเคนการเข้าถึงที่ออกโดยแพลตฟอร์มข้อมูลเฉพาะของ Microsoft</span><span class="sxs-lookup"><span data-stu-id="f5628-116">Here is an example of an access token that is issued by the Microsoft identity platform.</span></span>

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

<span data-ttu-id="f5628-117">เมื่อต้องการเรียก API ข้อมูล คุณต้องแนบโทเคนการเข้าถึงเป็นโทเคนผู้ถือสิทธิ์ไปยังหัวข้อการตรวจสอบในการร้องขอ HTTP ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f5628-117">To call the data API, you attach the access token as a bearer token to the authorization header in your HTTP request.</span></span> <span data-ttu-id="f5628-118">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="f5628-118">Here is an example.</span></span>

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a><span data-ttu-id="f5628-119">ลงทะเบียนแอปพลิเคชันใหม่โดยใช้พอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="f5628-119">Register a new application by using the Azure portal</span></span>

1. <span data-ttu-id="f5628-120">ล็อกอินไปยัง [พอร์ทัล Microsoft Azure](https://portal.azure.com) ที่มีบัญชีที่ทำงานหรือโรงเรียนหรือบัญชี Microsoft ส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="f5628-120">Sign in to the [Microsoft Azure portal](https://portal.azure.com) with a work or school account, or a personal Microsoft account.</span></span>

2. <span data-ttu-id="f5628-121">ถ้าบัญชีของคุณให้สิทธิการเข้าถึงแก่ผู้เช่ามากกว่าหนึ่งราย ให้เลือกบัญชีของคุณในมุมด้านขวาบน และตั้งค่ารอบของพอร์ทัลไปยังผู้เช่า Azure Active Directory (Azure AD) ที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="f5628-121">If your account gives you access to more than one tenant, select your account in the upper-right corner, and set your portal session to the Azure Active Directory (Azure AD) tenant that you want.</span></span>

3. <span data-ttu-id="f5628-122">ในบานหน้าต่างด้านซ้าย ให้เลือกบริการ **Azure Active Directory** แล้วเลือก **การลงทะเบียนแอป \> ลงทะเบียนใหม่**</span><span class="sxs-lookup"><span data-stu-id="f5628-122">In the left pane, select the **Azure Active Directory** service, and then select **App registrations \> New registration**.</span></span>

4. <span data-ttu-id="f5628-123">เมื่อหน้า**ลงทะเบียนแอปพลิเคชัน** ปรากฏขึ้น ให้ป้อนข้อมูลการลงทะเบียนของแอพลิเคชันของคุณ:</span><span class="sxs-lookup"><span data-stu-id="f5628-123">When the **Register an application** page appears, enter your application's registration information:</span></span>

    - <span data-ttu-id="f5628-124">**ชื่อ**: ให้ป้อนชื่อที่มีความหมายของแอปพลิเคชันที่จะแสดงต่อผู้ใช้แอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="f5628-124">**Name**: Enter a meaningful application name that will be shown to users of the app.</span></span>
    - <span data-ttu-id="f5628-125">**ชนิดบัญชีที่ได้รับการสนับสนุน**: เลือกชนิดบัญชีที่แอปของคุณควรสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="f5628-125">**Supported account types**: Select the types of accounts that your app should support.</span></span>

        | <span data-ttu-id="f5628-126">ชนิดบัญชีที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="f5628-126">Supported account types</span></span> | <span data-ttu-id="f5628-127">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="f5628-127">Description</span></span> |
        |-------------------------|-------------|
        | <span data-ttu-id="f5628-128">บัญชีในไดเรกทอรีขององค์กรนี้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f5628-128">Accounts in this organizational directory only</span></span> | <span data-ttu-id="f5628-129">เลือกตัวเลือกนี้ถ้าคุณกำลังสร้างแอปพลิเคชันสายธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="f5628-129">Select this option if you're building a line-of-business app.</span></span> <span data-ttu-id="f5628-130">ตัวเลือกนี้จะไม่พร้อมใช้งานจนกว่าคุณจะลงทะเบียนแอปในไดเรกทอรี</span><span class="sxs-lookup"><span data-stu-id="f5628-130">This option isn't available unless you're registering the app in a directory.</span></span><p><span data-ttu-id="f5628-131">ตัวเลือกนี้จะถูกแม็ปกับ **ผู้เช่า Azure AD คนเดียวเท่านั้น**</span><span class="sxs-lookup"><span data-stu-id="f5628-131">This option is mapped to **Azure AD only single-tenant**.</span></span></p><p><span data-ttu-id="f5628-132">ตัวเลือกนี้เป็นตัวเลือกเริ่มต้นยกเว้นว่าคุณกำลังลงทะเบียนแอปพลิเคภายนอกไดเรกทอรี</span><span class="sxs-lookup"><span data-stu-id="f5628-132">This option is the default option unless you're registering the app outside a directory.</span></span> <span data-ttu-id="f5628-133">ในกรณีนี้ ตัวเลือกเริ่มต้นคือผู้เช่า **Azure AD หลายรายและบัญชีส่วนบุคคล Microsoft**</span><span class="sxs-lookup"><span data-stu-id="f5628-133">In that case, the default option is **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p> |
        | <span data-ttu-id="f5628-134">บัญชีในไดเรกทอรีขององค์กรใดๆ</span><span class="sxs-lookup"><span data-stu-id="f5628-134">Accounts in any organizational directory</span></span> | <span data-ttu-id="f5628-135">เลือกตัวเลือกนี้เพื่อกำหนดเป้าหมายลูกค้าธุรกิจและการศึกษาทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f5628-135">Select this option to target all business and educational customers.</span></span><p><span data-ttu-id="f5628-136">ตัวเลือกนี้จะถูกแม็ปกับ **ผู้เช่า Azure AD มากกว่าหนึ่งคนเท่านั้น**</span><span class="sxs-lookup"><span data-stu-id="f5628-136">This option is mapped to **Azure AD only multi-tenant**.</span></span></p><p><span data-ttu-id="f5628-137">ถ้าคุณลงทะเบียนแอป **ผู้เช่า Azure AD รายเดียวเท่านั้น** คุณสามารถใช้เบลด **การรับรองความถูกต้อง** เพื่ออัพเดตเป็น **ผู้เช่า Azure AD มากกว่าหนึ่งรายเท่านั้น** และกลับไปยัง **ผู้เช่า Azure AD รายเดียวเท่านั้น**</span><span class="sxs-lookup"><span data-stu-id="f5628-137">If you registered the app as **Azure AD only single-tenant**, you can use the **Authentication** blade to update it to **Azure AD only multi-tenant** and then back to **Azure AD only single-tenant**.</span></span></p> |
        | <span data-ttu-id="f5628-138">บัญชีในไดเรกทอรีขององค์กรและบัญชี Microsoft ส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="f5628-138">Accounts in any organizational directory and personal Microsoft accounts</span></span> | <span data-ttu-id="f5628-139">เลือกตัวเลือกนี้เพื่อกำหนดเป้าหมายของกลุ่มลูกค้าที่กว้างที่สุด</span><span class="sxs-lookup"><span data-stu-id="f5628-139">Select this option to target the widest set of customers.</span></span><p><span data-ttu-id="f5628-140">ตัวเลือกนี้ถูกแม็ปโดย **ผู้เช่า Azure AD หลายรายเท่านั้นและบัญชีส่วนบุคคล Microsoft**</span><span class="sxs-lookup"><span data-stu-id="f5628-140">This option is mapped to **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p><p><span data-ttu-id="f5628-141">ถ้าคุณลงทะเบียนแอป **ผู้เช่า Azure AD หลายรายและบัญชี Microsoft ส่วนบุคคล** คุณจะไม่สามารถเปลี่ยนการตั้งค่านี้ในอินเทอร์เฟสผู้ใช้ (UI) ได้</span><span class="sxs-lookup"><span data-stu-id="f5628-141">If you registered the app as **Azure AD multi-tenant and personal Microsoft accounts**, you can't change this setting in the user interface (UI).</span></span> <span data-ttu-id="f5628-142">ในทางกลับกัน คุณต้องใช้ตัวแก้ไขรายการแอปพลิเคชันเพื่อเปลี่ยนชนิดบัญชีที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="f5628-142">Instead, you must use the application manifest editor to change the supported account types.</span></span></p> |

    - <span data-ttu-id="f5628-143">**การเปลี่ยนเส้นทาง URI (ตัวเลือก)** – เลือกชนิดของแอปที่คุณกำลังสร้าง **เว็บ** หรือ **ไคลเอนต์สาธารณะ (บนมือถือ & เดสก์ทอป)**</span><span class="sxs-lookup"><span data-stu-id="f5628-143">**Redirect URI (optional)** – Select the type of app that you're building: **Web** or **Public client (mobile & desktop)**.</span></span> <span data-ttu-id="f5628-144">ป้อน URI ที่เปลี่ยนเส้นทาง (หรือตอบกลับ URL)  สำหรับแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="f5628-144">Then enter the redirect URI (or reply URL) for the app.</span></span>

        - <span data-ttu-id="f5628-145">สำหรับแอปเว็บ ระบุ URL พื้นฐานของแอป</span><span class="sxs-lookup"><span data-stu-id="f5628-145">For web apps, provide the base URL of the app.</span></span> <span data-ttu-id="f5628-146">ตัวอย่างเช่น `http://localhost:31544` อาจเป็น URL สำหรับเว็บแอปพลิเคชันที่ดำเนินการบนเครื่องเฉพาะที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f5628-146">For example, `http://localhost:31544` might be the URL for a web app that runs on your local machine.</span></span> <span data-ttu-id="f5628-147">จากนั้น ผู้ใช้ใช้ URL นี้เพื่อล็อกอินไปยังแอปพลิเคชันไคลเอนต์ของเว็บ</span><span class="sxs-lookup"><span data-stu-id="f5628-147">Users then use this URL to sign in to a web client app.</span></span>
        - <span data-ttu-id="f5628-148">สำหรับแอปพลิเคชันไคลเอนต์สาธารณะให้ URL ที่ Azure AD ใช้เพื่อส่งคืนการตอบสนองโทเคน</span><span class="sxs-lookup"><span data-stu-id="f5628-148">For public client apps, provide the URI that Azure AD uses to return token responses.</span></span> <span data-ttu-id="f5628-149">ป้อนค่าที่เกี่ยวข้องกับแอปของคุณโดยเฉพาะเช่น`myapp://auth`</span><span class="sxs-lookup"><span data-stu-id="f5628-149">Enter a value that is specific to your app, such as `myapp://auth`.</span></span>

        <span data-ttu-id="f5628-150">เมื่อต้องการดูตัวอย่างเฉพาะสำหรับ web apps หรือแอปพลิเคชันดังเดิม ให้ดูที่ quickstarts ใน [แพลตฟอร์ม Microsoft identity (Azure Active Directory เดิมสำหรับนักพัฒนา)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts)</span><span class="sxs-lookup"><span data-stu-id="f5628-150">To see specific examples for web apps or native apps, see the quickstarts in [Microsoft identity platform (formerly Azure Active Directory for developers)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span></span>

5. <span data-ttu-id="f5628-151">ภายใต้ **สิทธิ์ของ API** ให้เลือก **เพิ่มสิทธิการได้รับอนุญาต**</span><span class="sxs-lookup"><span data-stu-id="f5628-151">Under **API permissions**, select **Add a permission**.</span></span> <span data-ttu-id="f5628-152">จากนั้น บนแท็บ **APIs องค์กรของฉันใช้** ให้ค้นหา **Dynamics 365 Human Resources** และเพิ่มสิทธิ์ **ผู้ใช้\_การเลียนแบบ** กับแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="f5628-152">Then, on the **APIs my organization uses** tab, search for **Dynamics 365 Human Resources**, and add the **user\_impersonation** permission to your app.</span></span> <span data-ttu-id="f5628-153">รหัสแอปพลิเคชันสำหรับทรัพยากรบุคคลคือ f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="f5628-153">The Application ID for Human Resources is f9be0c49-aa22-4ec6-911a-c5da515226ff.</span></span> <span data-ttu-id="f5628-154">ใช้รหัสนี้เพื่อให้แน่ใจว่าคุณได้เลือกแอปพลิเคชันที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="f5628-154">Use this ID to ensure you have chosen the correct application.</span></span>

6. <span data-ttu-id="f5628-155">เลือก **การลงทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="f5628-155">Select **Register**.</span></span>

   <span data-ttu-id="f5628-156">[![กำลังลงทะเบียนแอปใหม่ในพอร์ทัล Azure](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="f5628-156">[![Registering a new app in the Azure portal](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span></span>

<span data-ttu-id="f5628-157">Azure AD กำหนดรหัสแอปพลิเคชันเฉพาะ (รหัสไคลเอนต์) ให้กับแอปของคุณและ นำคุณไปยังหน้า **ภาพรวม** สำหรับแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="f5628-157">Azure AD assigns a unique application ID (client ID) to your app, and takes you to the **Overview** page for your app.</span></span> <span data-ttu-id="f5628-158">เพื่อเพิ่มความสามารถไปยังแอปของคุณ คุณสามารถเลือกการตั้งค่าคอนฟิกอื่นๆ เช่น ตัวเลือกสำหรับการสร้างแบรนด์ และสำหรับใบรับรองและความลับ</span><span class="sxs-lookup"><span data-stu-id="f5628-158">To add more capabilities to your app, you can select other configuration options, such as options for branding and for certificates and secrets.</span></span>

## <a name="retrieving-an-access-token"></a><span data-ttu-id="f5628-159">การดึงข้อมูลโทเคนการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="f5628-159">Retrieving an access token</span></span>

<span data-ttu-id="f5628-160">ข้อกำหนดในการดึงข้อมูลโทเคนการเข้าถึงสำหรับการเรียก API ข้อมูลทรัพยากรบุคคลจะขึ้นอยู่กับเทคโนโลยีที่คุณกำลังใช้ในการพัฒนาแอปพลิเคชันไคลเอนต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f5628-160">The specifics of how you retrieve an access token for calling the Human Resources data API will depend on what technologies you're using to develop your client application.</span></span> <span data-ttu-id="f5628-161">ตัวอย่างเช่น คุณอาจ [กำลังทดสอบกับยูทิลิตี้](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (เช่นบุรุษไปรษณีย์) การพัฒนาแอปพลิเคชันคอนโซล C# หรือการบริการเว็บ หรือการสร้างไคลเอนต์ javascript/TypeScript</span><span class="sxs-lookup"><span data-stu-id="f5628-161">For example, you might be [testing with a third party utility](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (such as Postman), developing a C# console application or web service, or building a javascript/TypeScript client.</span></span>

<span data-ttu-id="f5628-162">ตัวอย่างแอปพลิเคชันไคลเอนต์ C#:</span><span class="sxs-lookup"><span data-stu-id="f5628-162">Example C# client application:</span></span>
```C#
using System;
using System.Net.Http;
using System.Threading.Tasks;

// requires appropriate NuGet package references in the project
using Microsoft.IdentityModel.Clients.ActiveDirectory;

namespace TalentODataPoC
{
    class Program
    {
        // prereq: This client app must be registered in Azure Active Directory. The app must be
        // registered as requiring permission to the Dynamics 365 for Talent API (with the Dynamics
        // HCM Workload delegated permission).
        static string clientId = "4fc703ef-672c-4e2c-813f-2f9d29d726db"; // This value should be obtained from AAD and must match your registered app
        static string talentNamespaceUri = "";

        public static async Task CallTalentODataService()
        {
            // authority URI
            UriBuilder uri = new UriBuilder("https://login.microsoftonline.com/common");
            AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

            // request token for the resource we want to access (Human Resources). This will authenticate
            // the user and return an access token containing claims for the authenticated user.
            var authResult = await authenticationContext.AcquireTokenAsync(
                "http://hr.talent.dynamics.com", /*Talent app id or resource URI*/
                clientId, /*registered client app id*/
                new Uri("https://localhost"), /*redirect URI, as registered in your AAD app*/
                new PlatformParameters(PromptBehavior.SelectAccount));

            // create the authorization header, which needs to be passed in the Header of the HTTP Requests to Talent
            string authHeader = authResult.CreateAuthorizationHeader();

            // HINT: paste the JWT into https://jwt.ms to decode and view it
            Console.Write("authHeader: ");
            Console.WriteLine(authHeader);
            Console.WriteLine();

            HttpClient client = new HttpClient();
            client.DefaultRequestHeaders.Add("Authorization", authHeader);

            string s;

            Console.Write("Talent Namespace URI: ");
            Console.WriteLine(talentNamespaceUri);
            Console.WriteLine();

            // call the OData service to get JobType data from Talent
            var resultOdata = await client.GetAsync(talentNamespaceUri + "data/JobTypes");
            s = await resultOdata.Content.ReadAsStringAsync();
            Console.WriteLine(s);
            Console.WriteLine();
        }

        static void Main(string[] args)
        {
            Console.WriteLine();

            // if the user passes in a single parameter, assume it is the namespaceUri for Talent
            if (args.Length == 1)
            {
                talentNamespaceUri = args[0];
            } else if (args.Length == 0)
            {
                Console.WriteLine("Enter Talent URL including namespace.");
                Console.WriteLine("Example: https://aos-rts-sf-21454f9d830-prod-westus2.hr.talent.dynamics.com/namespaces/2328af1a-2d45-4c6a-99e3-12a4c3867dcf/");
                Console.Write("> ");
                talentNamespaceUri = Console.ReadLine();
                if (!talentNamespaceUri.EndsWith("/"))
                {
                    talentNamespaceUri = talentNamespaceUri + "/";
                }
            } else
            {
                Console.WriteLine("Unexpected Arguments");
                System.Environment.Exit(1);
            }

            Task t = Program.CallTalentODataService();
            t.Wait();
        }
    }
}
```

<span data-ttu-id="f5628-163">หลังจากที่คุณได้ดึงโทเคนการเข้าถึงแล้ว คุณจะผ่านโทเคนในส่วนหัวของการตรวจสอบเป็นโทเคนผู้ถือสิทธิ์โดยมีคำขอแต่ละรายการที่คุณจะส่งไปยัง API ข้อมูลดังที่อธิบายไว้ข้างต้น</span><span class="sxs-lookup"><span data-stu-id="f5628-163">Once you've retrieved an access token, you'll pass the token in the Authorization header as a bearer token with each request you send to the data API, as described above.</span></span>
