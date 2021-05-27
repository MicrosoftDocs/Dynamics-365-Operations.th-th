---
title: ไม่สามารถตั้งค่าคอนฟิกกลุ่มความปลอดภัยของโปรแกรมสร้างไซต์ Commerce ในระหว่างการปรับใช้ครั้งแรก
description: หัวข้อนี้จะแนะนําการแก้ไขปัญหาที่สามารถช่วยได้เมื่อกลุ่มรักษาความปลอดภัยของ Microsoft Azure Active Directory (Azure AD) สําหรับโปรแกรมสร้างไซต์ Commerce ไม่ปรากฏเป็นตัวเลือกเมื่อคุณสร้างส่วนประกอบอีคอมเมิร์ซใน Microsoft Dynamics Lifecycle Services (LCS) ในระหว่างการปรับใช้ผู้เช่าอีเมลใหม่
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d29e560d0f7b2bbc2415d7a0f6fe18f2ca17dc7c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020743"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a><span data-ttu-id="2ee60-103">ไม่สามารถตั้งค่าคอนฟิกกลุ่มความปลอดภัยของโปรแกรมสร้างไซต์ Commerce ในระหว่างการปรับใช้ครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="2ee60-103">Can't configure a security group for Commerce site builder during initial deployment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2ee60-104">หัวข้อนี้จะแนะนําการแก้ไขปัญหาที่สามารถช่วยได้เมื่อกลุ่มรักษาความปลอดภัยของ Microsoft Azure Active Directory (Azure AD) สําหรับโปรแกรมสร้างไซต์ Commerce ไม่ปรากฏเป็นตัวเลือกเมื่อคุณสร้างส่วนประกอบอีคอมเมิร์ซใน Microsoft Dynamics Lifecycle Services (LCS) ในระหว่างการปรับใช้ผู้เช่าอีเมลใหม่</span><span class="sxs-lookup"><span data-stu-id="2ee60-104">This topic provides troubleshooting guidance that can help when the Microsoft Azure Active Directory (Azure AD) security group for Commerce site builder doesn't appear as an option when you create e-commerce components in Microsoft Dynamics Lifecycle Services (LCS) during initial deployment of a new e-commerce tenant.</span></span>

## <a name="description"></a><span data-ttu-id="2ee60-105">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="2ee60-105">Description</span></span>

<span data-ttu-id="2ee60-106">เมื่อคุณสร้างส่วนประกอบของอีคอมเมิร์ซเป็นส่วนหนึ่งของกระบวนการปรับใช้ผู้เช่าอีคอมเมิร์ซใหม่ที่มีส่วนประกอบของโปรแกรมสร้างไซต์ Commerce กลุ่มรักษาความปลอดภัย Azure AD จะไม่ปรากฎขึ้นเป็นตัวเลือกในกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="2ee60-106">When you create the e-commerce components as part of the process of deploying a new e-commerce tenant that includes the Commerce site builder component, the Azure AD security group doesn't appear as an option in the dialog box.</span></span>

## <a name="resolution"></a><span data-ttu-id="2ee60-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="2ee60-107">Resolution</span></span>

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a><span data-ttu-id="2ee60-108">เตรียมใช้งานไซต์อีคอมเมิร์ซให้กับผู้ใช้ในผู้เช่าที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="2ee60-108">Provision the e-commerce site with a user in the correct tenant</span></span>

1. <span data-ttu-id="2ee60-109">ไปที่ [พอร์ทัล Azure](https://portal.azure.com/)</span><span class="sxs-lookup"><span data-stu-id="2ee60-109">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="2ee60-110">ภายใต้ผู้เช่าที่เตรียมใช้งานโครงการ LCS สำหรับไซต์อีคอมเมิร์ซของคุณ ให้ปฏิบัติตามคําแนะนํา [การสร้างกลุ่มพื้นฐานและเพิ่มสมาชิกโดยใช้ Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)</span><span class="sxs-lookup"><span data-stu-id="2ee60-110">Under the tenant that the LCS project for your e-commerce site was provisioned for, follow the instructions in [Create a basic group and add members using Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span></span>
1. <span data-ttu-id="2ee60-111">ไปที่ [LCS ](https://lcs.dynamics.com/) และลงชื่อเข้าใช้งานโดยใช้บัญชีที่ใช้ผู้เช่าเดียวกันกับกลุ่มรักษาความปลอดภัย Azure AD ที่คุณเพิ่งสร้างขึ้นร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="2ee60-111">Go to [LCS](https://lcs.dynamics.com/), and sign in by using an account that shares the same tenant as the Azure AD security group that you just created.</span></span> <span data-ttu-id="2ee60-112">บัญชีต้องมีสิทธิ์เข้าดูกลุ่มรักษาความปลอดภัย Azure AD</span><span class="sxs-lookup"><span data-stu-id="2ee60-112">The account must have access to view the Azure AD security group.</span></span>
1. <span data-ttu-id="2ee60-113">ทำขั้นตอนการตั้งค่าเพื่อตั้งค่าคอนฟิกไซต์อีคอมเมิร์ซให้เสร็จ</span><span class="sxs-lookup"><span data-stu-id="2ee60-113">Complete the setup steps to configure the e-commerce site.</span></span> <span data-ttu-id="2ee60-114">เมื่อคุณเตรียมใช้งานส่วนประกอบของอีคอมเมิร์ซ ขณะนี้กลุ่มรักษาความปลอดภัยควรปรากฏเป็นตัวเลือกในกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="2ee60-114">When you provision the e-commerce components, the security group should now appear as an option in the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="2ee60-115">เพื่อให้แน่ใจว่าฟิลด์ในกล่องโต้ตอบจะเติมด้วยรายการกลุ่มความปลอดภัย คุณต้องเลือก **ป้อน** หลังจากที่คุณป้อนชื่อของกลุ่มรักษาความปลอดภัย Azure AD ที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="2ee60-115">To ensure that the field in the dialog box is filled with the list of security groups, you must select **Enter** after you enter the name of the Azure AD security group that you created.</span></span> <span data-ttu-id="2ee60-116">ผลการค้นหาจะแสดงรายการกลุ่มความปลอดภัย Azure AD ทั้งหมดที่ขึ้นต้นด้วยข้อความการค้นหา และที่ผู้ใช้มีสิทธิ์เข้าถึง</span><span class="sxs-lookup"><span data-stu-id="2ee60-116">The search results will list all the Azure AD security groups that start with the search text, and that the user has access to.</span></span> <span data-ttu-id="2ee60-117">คุณสามารถใช้เงื่อนไขการค้นหาสั้นๆ เพื่ออนุญาตให้ใช้ผลการค้นหาที่กว้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="2ee60-117">You can use a shorter search term to allow for broader search results.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ee60-118">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="2ee60-118">Additional resources</span></span>

[<span data-ttu-id="2ee60-119">การสร้างกลุ่มพื้นฐานและเพิ่มสมาชิกโดยใช้ Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="2ee60-119">Create a basic group and add members using Azure Active Directory</span></span>](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[<span data-ttu-id="2ee60-120">ปรับใช้ผู้เช่าอีคอมเมิร์ซใหม่</span><span class="sxs-lookup"><span data-stu-id="2ee60-120">Deploy a new e-commerce tenant</span></span>](../deploy-ecommerce-site.md)