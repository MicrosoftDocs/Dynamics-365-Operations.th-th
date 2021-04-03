---
title: ลิงค์การลงชื่อเข้าใช้จะเปลี่ยนเส้นทางกลับไปยังไซต์อีคอมเมิร์ซ
description: หัวข้อนี้มีการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อลิงค์การลงชื่อเข้าใช้เปลี่ยนเส้นทางกลับไปที่ไซต์อีคอมเมิร์ซ แทนที่จะไปที่หน้าลงชื่อเข้าใช้
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 36f10c9f68570a6c67da6b4b6e4155f4634f633a
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585547"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a><span data-ttu-id="7ac13-103">ลิงค์การลงชื่อเข้าใช้จะเปลี่ยนเส้นทางกลับไปยังไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="7ac13-103">Sign-in link redirects back to an e-commerce site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7ac13-104">หัวข้อนี้มีการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อลิงค์การลงชื่อเข้าใช้เปลี่ยนเส้นทางกลับไปที่ไซต์อีคอมเมิร์ซ แทนที่จะไปที่หน้าลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="7ac13-104">This topic provides troubleshooting guidance that can help when a sign-in link redirects back to the e-commerce site instead of going to the sign-in page.</span></span>

## <a name="description"></a><span data-ttu-id="7ac13-105">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="7ac13-105">Description</span></span>

<span data-ttu-id="7ac13-106">หลังจากที่คุณตั้งค่าคอนฟิกผู้เช่า Microsoft Azure Active Directory B2C (Azure AD B2C) ใหม่ในโปรแกรมสร้างไซต์ Commerce แล้ว ผู้ใช้ที่เลือกลิงค์  **การลงชื่อเข้าใช้** จะเปลี่ยนเส้นทางกลับไปที่หน้าเชื่อมโยงสินค้าอีคอมเมิร์ซหลักโดยไม่ไปที่หน้าการลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="7ac13-106">After you configure a new Microsoft Azure Active Directory B2C (Azure AD B2C) tenant in Commerce site builder, users who select the **Sign in** link are redirected back to the main e-commerce landing page without going to the sign-in page.</span></span>

## <a name="resolution"></a><span data-ttu-id="7ac13-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="7ac13-107">Resolution</span></span>

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a><span data-ttu-id="7ac13-108">ยืนยันว่าการตอบ URL ได้รับการตั้งค่าคอนฟิกในแอปพลิเคชัน Azure AD B2C อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="7ac13-108">Confirm that the reply URL is correctly configured in the Azure AD B2C application</span></span>

<span data-ttu-id="7ac13-109">ในการยืนยันว่าการตอบ URL ได้รับการตั้งค่าคอนฟิกในแอปพลิเคชัน Azure AD B2C อย่างถูกต้อง ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7ac13-109">To confirm that the reply URL is correctly configured in the Azure AD B2C application, follow these steps.</span></span>

1. <span data-ttu-id="7ac13-110">ไปที่ [พอร์ทัล Azure](https://portal.azure.com/)</span><span class="sxs-lookup"><span data-stu-id="7ac13-110">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="7ac13-111">เลือกแอปพลิเคชัน Azure AD B2C ที่คุณสร้างขึ้นเพื่อการเข้าถึงไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="7ac13-111">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="7ac13-112">เลือกแอปพลิเคชันที่คุณสร้างขึ้นระหว่างการตั้งค่า Azure AD B2C</span><span class="sxs-lookup"><span data-stu-id="7ac13-112">Select the application that you created during the Azure AD B2C setup.</span></span>
1. <span data-ttu-id="7ac13-113">ภายใต้ **การตอบ URL** ตรวจสอบให้แน่ใจว่ารายการมีรายการทั้ง URL โดเมนไซต์และ URL ที่สร้างขึ้นโดยอีคอมเมิร์ซดังที่แสดงในตัวอย่างในภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7ac13-113">Under **Reply URL**, make sure that the list includes entries for both the site domain URL and the e-commerce-generated URL, as shown in the example in the following illustration.</span></span>

    ![รายการการตอบ URL Azure AD B2C](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> <span data-ttu-id="7ac13-115">ทั้ง URL โดเมนไซต์และ URL ที่สร้างโดยอีคอมเมิร์ซต้องอยู่ในรูปแบบ URL ที่ถูกต้องซึ่งไม่รวมเครื่องหมายทับนำหน้าหรือต่อท้าย</span><span class="sxs-lookup"><span data-stu-id="7ac13-115">Both the site domain URL and the e-commerce-generated URL must be in a valid URL format that doesn't include leading or trailing slashes.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7ac13-116">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="7ac13-116">Additional resources</span></span>

[<span data-ttu-id="7ac13-117">ลงทะเบียนแอปพลิเคชันเว็บใน Azure Active Directory B2C</span><span class="sxs-lookup"><span data-stu-id="7ac13-117">Register a web application in Azure Active Directory B2C</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[<span data-ttu-id="7ac13-118">ตั้งค่าผู้เช่า B2C ใน Commerce</span><span class="sxs-lookup"><span data-stu-id="7ac13-118">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)
