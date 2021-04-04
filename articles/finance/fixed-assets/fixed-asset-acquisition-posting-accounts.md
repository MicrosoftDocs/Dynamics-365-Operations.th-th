---
title: บัญชีการลงรายการการซื้อสินทรัพย์ถาวร
description: บทความนี้อธิบายวิธีการตั้งค่าบัญชีแยกประเภททั่วไปที่ลงรายการบัญชีสำหรับสินทรัพย์ที่ซื้อสินทรัพย์
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a340df57a6073c6d9b6f2cdaadbf8f21fc11649
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241053"
---
# <a name="fixed-asset-acquisition-posting-accounts"></a><span data-ttu-id="7d27a-103">บัญชีการลงรายการการซื้อสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="7d27a-103">Fixed asset acquisition posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d27a-104">บทความนี้อธิบายวิธีการตั้งค่าบัญชีแยกประเภททั่วไปที่ลงรายการบัญชีสำหรับสินทรัพย์ที่ซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="7d27a-104">This article explains how to set up general ledger posting accounts for acquiring assets.</span></span>

<span data-ttu-id="7d27a-105">บัญชีที่ใช้สำหรับการลงรายการการซื้อสินทรัพย์ถาวรอาจแตกต่างกันไป โดยขึ้นอยู่กับวิธีการที่ใช้เพื่อซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="7d27a-105">Accounts used for posting fixed asset acquisitions may vary depending upon the method used to acquire the asset.</span></span> <span data-ttu-id="7d27a-106">ในหน้าโพรไฟล์การลงรายการบัญชีสินทรัพย์ถาวรบนแท็บบัญชีแยกประเภท เลือกการซื้อสินทรัพย์ และการปรับปรุงการซื้อสินทรัพย์เพื่อตั้งค่าบัญชีสินทรัพย์ถาวรเพื่อลงรายการบัญชีในบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="7d27a-106">On the Fixed asset posting profiles page, on the Ledger accounts tab, select Acquisition and Acquisition adjustment to set up fixed asset accounts to post to the ledger.</span></span> 

<span data-ttu-id="7d27a-107">ในสมุดรายวัน และใบสั่งซื้อ บัญชีแยกประเภท คือบัญชีงบดุลที่ใช้โดยทั่วไป ซึ่งมีการเดบิตมูลค่าการซื้อของสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="7d27a-107">In journals and on purchase orders, Ledger account is typically the balance sheet account, where the acquisition value of the new fixed asset is debited.</span></span> <span data-ttu-id="7d27a-108">บัญชีนี้จะไม่แสดงในสมุดรายวัน และไม่สามารถแทนที่ในธุรกรรมได้</span><span class="sxs-lookup"><span data-stu-id="7d27a-108">This account is not displayed in the journal and cannot be replaced in transactions.</span></span> 

<span data-ttu-id="7d27a-109">บัญชีตรงข้ามจะเป็นบัญชีงบดุลด้วย</span><span class="sxs-lookup"><span data-stu-id="7d27a-109">Offset account is also a balance sheet account.</span></span> <span data-ttu-id="7d27a-110">ในสมุดรายวันทั่วไป และ ในสมุดรายวันสินทรัพย์ถาวร บัญชีนี้มักจะเป็นบัญชีธนาคารที่ใช้ในการชำระค่าจ้างสำหรับการซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="7d27a-110">In the general journal and in the fixed assets journal, this account often will be the bank account that is used to pay for the acquisition of the asset.</span></span> <span data-ttu-id="7d27a-111">บัญชีตรงข้ามเป็นบัญชีเริ่มต้น ซึ่งมีการแนะนำอยู่ในสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="7d27a-111">The offset account is a default account, which is suggested in the journals.</span></span> <span data-ttu-id="7d27a-112">สามารถเปลี่ยนในสมุดรายวันไปยังบัญชีอื่นใดจากผังบัญชี หรือไปยังบัญชีผู้จัดจำหน่าย ถ้าซื้อสินทรัพย์ถาวรมาจากผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="7d27a-112">It can be changed in the journal to any other account from the chart of accounts or to a vendor account, if the fixed asset was purchase from a vendor.</span></span> 

<span data-ttu-id="7d27a-113">เมื่อใช้สมุดรายวันใบแจ้งหนี้หรือใบสั่งซื้อในบัญชี สำหรับการได้มาซึ่งสินทรัพย์ถาวร บัญชีตรงข้ามสำหรับธุรกรรมสินทรัพย์ถาวรจะถูกแทนที่ด้วยบัญชีผู้จัดจำหน่าย ที่เลือกไว้สำหรับธุรกรรมนั้น</span><span class="sxs-lookup"><span data-stu-id="7d27a-113">When Invoice journal or Purchase orders in Accounts payable are used for fixed asset acquisitions, the offset account for the fixed asset transaction is replaced by the vendor account that is selected for the transaction.</span></span>

<span data-ttu-id="7d27a-114">สำหรับการลงรายการบัญชีการได้มาซึ่งสินทรัพย์ที่โดยใช้สมุดรายวันในบัญชีแยกประเภททั่วไป สินทรัพย์ถาวรไม่ได้ซื้อมาจากแหล่งภายนอก แต่โอนย้ายมาจากสินค้าคงคลังของบริษัทเอง</span><span class="sxs-lookup"><span data-stu-id="7d27a-114">For acquisitions posted using the Inventory to fixed assets journal in General ledger, the fixed asset is not bought from external sources, but transferred from the company's own inventory.</span></span> <span data-ttu-id="7d27a-115">ดังนั้น บัญชีตรงข้ามจึงเป็นบัญชีการตัดสินค้าจากคลังสำหรับสินค้าคงคลังในการบริหารสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="7d27a-115">Therefore, the offset account is an inventory issue account for the inventory item in Inventory management.</span></span>

<span data-ttu-id="7d27a-116">สำหรับข้อมูลเพิ่มเติม ดู [ซื้อสินทรัพย์ผ่านการจัดซื้อ](acquire-assets-procurement.md)</span><span class="sxs-lookup"><span data-stu-id="7d27a-116">For more information, see [Acquire assets through procurement](acquire-assets-procurement.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]