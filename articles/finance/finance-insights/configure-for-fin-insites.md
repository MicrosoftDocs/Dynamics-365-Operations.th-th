---
title: การตั้งค่าคอนฟิกสำหรับข้อมูลเชิงลึก Finance (พรีวิว)
description: หัวข้อนี้จะอธิบายขั้นตอนการตั้งค่าคอนฟิกที่จะช่วยให้ระบบของคุณสามารถใช้ความสามารถที่มีอยู่ในข้อมูลเชิงลึก Finance ได้
author: ShivamPandey-msft
ms.date: 11/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 54117c009cfeb7307938cc6bd43e774ccfedcfb1
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908841"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="f130b-103">การตั้งค่าคอนฟิกสำหรับข้อมูลเชิงลึก Finance</span><span class="sxs-lookup"><span data-stu-id="f130b-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f130b-104">ข้อมูลเชิงลึก Finance รวมฟังก์ชันจาก Microsoft Dynamics 365 Finance พร้อมกับ Microsoft Dataverse, Azure และ AI Builder เพื่อให้เครื่องมือการคาดการณ์ที่มีประสิทธิภาพสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="f130b-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="f130b-105">หัวข้อนี้จะอธิบายขั้นตอนการตั้งค่าคอนฟิกที่จะช่วยให้ระบบของคุณสามารถใช้ความสามารถที่มีอยู่ในข้อมูลเชิงลึก Finance ได้</span><span class="sxs-lookup"><span data-stu-id="f130b-105">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="f130b-106">ปรับใช้ Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="f130b-106">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="f130b-107">ปรับใช้สภาพแวดล้อมโดยการทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="f130b-107">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="f130b-108">ใน Microsoft Dynamics Lifecycle Services (LCS) สร้างหรืออัปเดตข้อมูลสภาพแวดล้อม Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="f130b-108">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="f130b-109">สภาพแวดล้อมต้องมีแอปรุ่น 10.0.11/Platform update 35 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="f130b-109">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="f130b-110">สภาพแวดล้อมต้องมีสภาพแวดล้อมที่มีความพร้อมใช้งานสูง (HA) ใน Sandbox</span><span class="sxs-lookup"><span data-stu-id="f130b-110">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="f130b-111">(สภาพแวดล้อมชนิดนี้เรียกอีกอย่างว่า สภาพแวดล้อมระดับ 2) สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การวางแผนสภาพแวดล้อม](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)</span><span class="sxs-lookup"><span data-stu-id="f130b-111">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="f130b-112">ถ้าคุณกำลังใช้ข้อมูลสาธิต Contoso คุณจะต้องใช้ข้อมูลตัวอย่างเพิ่มเติมเพื่อใช้คุณลักษณะการคาดการณ์การชำระเงินของลูกค้า การคาดการณ์กระแสเงินสด และการคาดการณ์งบประมาณ</span><span class="sxs-lookup"><span data-stu-id="f130b-112">If you're using Contoso demo data, you will require additional sample data to use the Customer payment predictions, Cash flow forecasts, and Budget forecasts features.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="f130b-113">ตั้งค่าคอนฟิก Dataverse</span><span class="sxs-lookup"><span data-stu-id="f130b-113">Configure Dataverse</span></span>

<span data-ttu-id="f130b-114">คุณสามารถดำเนินการขั้นตอนการตั้งค่าคอนฟิกด้วยตนเองที่ติดตามให้เสร็จสมบูรณ์ หรือคุณสามารถเพิ่มความเร็วในกระบวนการตั้งค่าคอนฟิกได้โดยใช้สคริปต์ Windows PowerShell ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="f130b-114">You can complete the manual configuration steps that follow, or you can speed up the configuration process by using the Windows PowerShell script that is provided.</span></span> <span data-ttu-id="f130b-115">เมื่อสคริปต์ PowerShell ทำงานเสร็จเรียบร้อยแล้ว จะช่วยให้คุณสามารถใช้ค่าเพื่อตั้งค่าคอนฟิกข้อมูลเชิงลึก Finance</span><span class="sxs-lookup"><span data-stu-id="f130b-115">When the PowerShell script has finished running, it will give you values to use to configure Finance insights.</span></span> 

> [!NOTE]
> <span data-ttu-id="f130b-116">เปิด PowerShell บนพีซีของคุณเพื่อรันสคริปต์</span><span class="sxs-lookup"><span data-stu-id="f130b-116">Open PowerShell on your PC to run the script.</span></span> <span data-ttu-id="f130b-117">คุณอาจต้องใช้ PowerShell รุ่น 5</span><span class="sxs-lookup"><span data-stu-id="f130b-117">You may need PowerShell version 5.</span></span> <span data-ttu-id="f130b-118">ตัวเลือก Microsoft Azure CLI "ทดลองใช้" อาจไม่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="f130b-118">The Microsoft Azure CLI "Try it" option may not work.</span></span>

# <a name="manual-configuration-steps"></a>[<span data-ttu-id="f130b-119">ขั้นตอนการตั้งค่าคอนฟิกด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="f130b-119">Manual configuration steps</span></span>](#tab/configuration-steps)

1. <span data-ttu-id="f130b-120">เปิด [ศูนย์การจัดการ Power Platform](https://admin.powerplatform.microsoft.com/) และปฏิบัติตามขั้นตอนต่อไปนี้เพื่อสร้างสภาพแวดล้อม Dataverse ใหม่ในผู้เช่า Active Directory เดียวกัน:</span><span class="sxs-lookup"><span data-stu-id="f130b-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="f130b-121">เปิดหน้า **สภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="f130b-121">Open the **Environments** page.</span></span>

        <span data-ttu-id="f130b-122">[![หน้าสภาพแวดล้อม](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="f130b-122">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="f130b-123">เลือก **สภาพแวดล้อมใหม่**</span><span class="sxs-lookup"><span data-stu-id="f130b-123">Select **New environment**.</span></span>
    3. <span data-ttu-id="f130b-124">ในฟิลด์ **ชนิด** เลือก **Sandbox**</span><span class="sxs-lookup"><span data-stu-id="f130b-124">In the **Type** field, select **Sandbox**.</span></span>
    4. <span data-ttu-id="f130b-125">ตั้งค่าตัวเลือก **สร้างฐานข้อมูล** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="f130b-125">Set the **Create Database** option to **Yes**.</span></span>
    5. <span data-ttu-id="f130b-126">เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="f130b-126">Select **Next**.</span></span>
    6. <span data-ttu-id="f130b-127">เลือกภาษาและสกุลเงินสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="f130b-127">Select the language and currency for your organization.</span></span>
    7. <span data-ttu-id="f130b-128">ยอมรับค่าเริ่มต้นสำหรับฟิลด์อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="f130b-128">Accept the default values for the other fields.</span></span>
    8. <span data-ttu-id="f130b-129">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f130b-129">Select **Save**.</span></span>
    9. <span data-ttu-id="f130b-130">รีเฟรชหน้า **สภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="f130b-130">Refresh the **Environments** page.</span></span>
    10. <span data-ttu-id="f130b-131">รอจนกว่าค่าของฟิลด์ **สถานะ** จะถูกอัปเดตเป็น **พร้อม**</span><span class="sxs-lookup"><span data-stu-id="f130b-131">Wait until the value of the **State** field is updated to **Ready**.</span></span>
    11. <span data-ttu-id="f130b-132">จดบันทึกรหัสองค์กร Dataverse</span><span class="sxs-lookup"><span data-stu-id="f130b-132">Make a note of the Dataverse organization ID.</span></span>
    12. <span data-ttu-id="f130b-133">เลือกสภาพแวดล้อม แล้วจากนั้น เลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="f130b-133">Select the environment, and then select **Settings**.</span></span>
    13. <span data-ttu-id="f130b-134">เลือก **ทรัพยากร \>การตั้งค่าดั้งเดิมทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="f130b-134">Select **Resources \> All Legacy Settings**.</span></span>
    14. <span data-ttu-id="f130b-135">บนแถบนำทางบนสุด ให้เลือก **การตั้งค่า** แล้วจากนั้น เลือก **การเลือกกำหนด**</span><span class="sxs-lookup"><span data-stu-id="f130b-135">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    15. <span data-ttu-id="f130b-136">เลือก **ทรัพยากรของนักพัฒนา**</span><span class="sxs-lookup"><span data-stu-id="f130b-136">Select **Developer Resources**.</span></span>
    16. <span data-ttu-id="f130b-137">คัดลอกค่า **รหัสองค์กร Dataverse**</span><span class="sxs-lookup"><span data-stu-id="f130b-137">Copy the **Dataverse organization ID** value.</span></span>
    17. <span data-ttu-id="f130b-138">ในแถบที่อยู่ของเบราว์เซอร์ ให้จดบันทึก URL ขององค์กร Dataverse</span><span class="sxs-lookup"><span data-stu-id="f130b-138">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="f130b-139">ตัวอย่างเช่น URL อาจเป็น `https://org42b2b3d3.crm.dynamics.com`</span><span class="sxs-lookup"><span data-stu-id="f130b-139">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

2. <span data-ttu-id="f130b-140">ถ้าคุณวางแผนที่จะใช้คุณลักษณะการคาดการณ์กระแสเงินสดหรือคุณลักษณะการคาดการณ์งบประมาณ ให้ทำตามขั้นตอนต่อไปนี้เพื่ออัปเดตการจำกัดคำอธิบายสำหรับองค์กรของคุณเป็นอย่างน้อย 50 เมกะไบต์ (MB):</span><span class="sxs-lookup"><span data-stu-id="f130b-140">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="f130b-141">เปิด [พอร์ทัล Power Apps](https://make.powerapps.com)</span><span class="sxs-lookup"><span data-stu-id="f130b-141">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="f130b-142">เลือกสภาพแวดล้อมที่คุณเพิ่งสร้าง แล้วจากนั้น เลือก **การตั้งค่าขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="f130b-142">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="f130b-143">เลือก **การตั้งค่า \> การตั้งค่าคอนฟิกอีเมล**</span><span class="sxs-lookup"><span data-stu-id="f130b-143">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="f130b-144">เปลี่ยนค่าของฟิลด์ **ขนาดไฟล์สูงสุด** เป็น **51,200**</span><span class="sxs-lookup"><span data-stu-id="f130b-144">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="f130b-145">(ค่าจะแสดงเป็นกิโลไบต์ \[KB\])</span><span class="sxs-lookup"><span data-stu-id="f130b-145">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="f130b-146">เลือก **ตกลง** เพื่อบันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="f130b-146">Select **OK** to save your changes.</span></span>

# <a name="windows-powershell-configuration-script"></a>[<span data-ttu-id="f130b-147">สคริปต์การตั้งค่าคอนฟิก Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f130b-147">Windows PowerShell configuration script</span></span>](#tab/powershell-configuration-script)

```azurecli-interactive
Write-Output 'The following modules need to be present for execution of this script:'
Write-Output '  Microsoft.PowerApps.Administration.PowerShell'
Write-Output '  Microsoft.PowerApps.PowerShell'
Write-Output '  Microsoft.Xrm.Tooling.CrmConnector.PowerShell'

try {
    $moduleConsent = Read-Host 'Is it ok to install or update these modules as needed? (yes/no)'
    if ($moduleConsent -ne 'yes' -and $moduleConsent -ne 'y') {
        Write-Warning 'User declined to install required modules.'
        return
    }

    $module = 'Microsoft.PowerApps.Administration.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '2.0.61' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '2.0.61' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.PowerApps.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '1.0.9' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '1.0.9' -AllowClobber -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.Xrm.Tooling.CrmConnector.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '3.3.0.892' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '3.3.0.892' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    Write-Output '================================================================================='

    $useMfa = $false
    $useMfaPrompt = Read-Host "Does your organization require the use of multi-factor authentication? (yes/no)"
    if ($useMfaPrompt -eq 'yes' -or $useMfaPrompt -eq 'y') {
        $useMfa = $true
    }
    if(-not $useMfa) {
        $credential = Get-Credential -Message 'Power Apps Credential'
    }

    $orgFriendlyName = Read-Host "Enter the name of the CDS Organization to use or create: (blank for 'FinanceInsightsOrg')"
    if ($orgFriendlyName.Trim() -eq '') {
        $orgFriendlyName = 'FinanceInsightsOrg'
    }

    $isDefaultOrgPrompt = Read-Host ("Is '" + $orgFriendlyName + "' the default organization for your tenant? (yes/no)")
    if ($isDefaultOrgPrompt -eq 'yes' -or $isDefaultOrgPrompt -eq 'y') {
        $isDefaultOrg = $true
    }

    if ($credential) {
        Add-PowerAppsAccount -Username $credential.UserName -Password $credential.Password
    }
    else {
        Add-PowerAppsAccount
    }

    if ($isDefaultOrg) {
        $orgMatch = ('(default)')
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { $_.IsDefault -eq $true })
    }
    else {
        $orgMatch = ('{0} (*)' -f $orgFriendlyName)
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.IsDefault -eq $false -and ($_.DisplayName -eq $orgFriendlyName -or $_.DisplayName -like $orgMatch)) })
    }

    $getCrmOrgParams = @{ 'OnlineType' = 'Office365' }
    if ($credential) {
        $getCrmOrgParams.Credential = $credential
    }

    if ($null -eq $environment) {
        Write-Output '================================================================================='
        Write-Output 'PowerApps environment not found. A new one will be provisioned.'

        $invalid = 'invalid'

        $location = $invalid
        $cdsLocations = (Get-AdminPowerAppEnvironmentLocations | Select-Object LocationName).LocationName
        while (-not ($location -in $cdsLocations)) {
            $location = (Read-Host -Prompt "Enter the location in which to create the new PowerApps environment: ('help' to see values)")
            if ($location -eq 'help') {
                $cdsLocations
            }
        }

        $currency = $invalid
        $cdsCurrencies = (Get-AdminPowerAppCdsDatabaseCurrencies -Location $location | Select-Object CurrencyName).CurrencyName
        while ($currency -ne '' -and -not ($currency -in $cdsCurrencies)) {
            $currency = (Read-Host -Prompt "Enter the currency to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($currency -eq 'help') {
                $cdsCurrencies
            }
        }

        $language = $invalid
        $cdsLanguages = (Get-AdminPowerAppCdsDatabaseLanguages -Location $location | Select-Object LanguageName, LanguageDisplayName)
        while ($language -ne '' -and -not ($language -in $cdsLanguages.LanguageName)) {
            $language = (Read-Host -Prompt "Enter the language name to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($language -eq 'help') {
                $cdsLanguages | Format-Table -Property LanguageName, LanguageDisplayName
            }
        }

        Write-Output 'Provisioning PowerApps environment. This may take several minutes.'

        $sleep = 15

        $envParams = @{ 'DisplayName' = $orgFriendlyName; 'EnvironmentSku' = 'Sandbox'; 'ProvisionDatabase' = $true; 'Location' = $location; 'WaitUntilFinished' = $true }
        if ($language.Trim() -ne '') {
            $envParams.LanguageName = $language
        }
        if ($currency.Trim() -ne '') {
            $envParams.CurrencyName = $currency
        }
        $newEnvResult = New-AdminPowerAppEnvironment @envParams
        if (($null -eq $newEnvResult) -or ($newEnvResult.CommonDataServiceDatabaseProvisioningState -ne 'Succeeded')) {
            Write-Warning 'Failed to create to PowerApps environment'
            if ($null -ne $newEnvResult) {
                $newEnvResult
            }
        }
        else {
            $environment = $null
            $retryCount = 0
            while (($null -eq $environment) -and ($retryCount -lt 5)) {
                Start-Sleep -Seconds $sleep
                $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.DisplayName -like $orgMatch) })
            }
            Write-Output ("Provisioned PowerApps environment with name: '" + $environment.DisplayName + "'")
        }

        Write-Output 'Waiting for CDS organization provisioning. This may take several minutes.'
        if (-not $credential) {
            $sleep = 120
            Write-Output 'You may be prompted for credentials multiple times while checking the status of the provisioning.'
        }

        while ($null -eq $crmOrg) {
            Start-Sleep -Seconds $sleep
            $crmOrg = (Get-CrmOrganizations @getCrmOrgParams) | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }
    else {
        $crmOrgs = Get-CrmOrganizations @getCrmOrgParams
        if ($UseDefaultOrganization -eq $true) {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -match $orgMatch }
        }
        else {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }

    Write-Output '================================================================================='
    Write-Output 'Values for PowerAI LCS Add-In:'
    Write-Output ("  CDS organization url:             " + $crmOrg.WebApplicationUrl)
    Write-Output ("  CDS organization ID:              " + $crmOrg.OrganizationId)
}
catch {
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $_.Exception.InnerException
    while ($null -ne $inner) {
        Write-Output 'Inner Exception:'
        Write-Error $_.Exception.Message
        Write-Warning $_.Exception.StackTrace
        $inner = $inner.InnerException
    }
}
```
---

## <a name="configure-the-azure-setup"></a><span data-ttu-id="f130b-148">ตั้งค่าคอนฟิกการตั้งค่า Azure</span><span class="sxs-lookup"><span data-stu-id="f130b-148">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="f130b-149">ป้อนรหัสไดเรกทอรี Dataverse และรหัสวัตถุ Azure AD ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="f130b-149">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="f130b-150">ป้อนรหัสไดเรกทอรี Dataverse:</span><span class="sxs-lookup"><span data-stu-id="f130b-150">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="f130b-151">เปิด [พอร์ทัล Azure](https://portal.azure.com)</span><span class="sxs-lookup"><span data-stu-id="f130b-151">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="f130b-152">ลงชื่อเข้าใช้โดยใช้รหัสผู้ใช้ที่ใช้ในการสร้างสภาพแวดล้อม Dataverse</span><span class="sxs-lookup"><span data-stu-id="f130b-152">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="f130b-153">ไปที่ **Azure Active Directory**</span><span class="sxs-lookup"><span data-stu-id="f130b-153">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="f130b-154">คัดลอกค่า **รหัสผู้เช่า**</span><span class="sxs-lookup"><span data-stu-id="f130b-154">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="f130b-155">ป้อนรหัสวัตถุ Azure Active Directory (Azure AD) ของผู้ใช้:</span><span class="sxs-lookup"><span data-stu-id="f130b-155">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="f130b-156">ใน [พอร์ทัล Azure](https://portal.azure.com) ให้ไปที่ **ผู้ใช้** และค้นหาผู้ใช้ตามที่อยู่อีเมล</span><span class="sxs-lookup"><span data-stu-id="f130b-156">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="f130b-157">เลือกชื่อของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="f130b-157">Select the user's name.</span></span>
    3. <span data-ttu-id="f130b-158">คัดลอกค่า **รหัสวัตถุ**</span><span class="sxs-lookup"><span data-stu-id="f130b-158">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="f130b-159">ใช้ Azure Cloud Shell เพื่อตั้งค่าทรัพยากร Data Lake ของข้อมูลเชิงลึก Finance</span><span class="sxs-lookup"><span data-stu-id="f130b-159">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="f130b-160">ใช้สคริปต์ Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f130b-160">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="f130b-161">มีการให้สคริปต์ Windows PowerShell ไว้ เพื่อให้คุณสามารถตั้งค่าทรัพยากร Azure ที่อธิบายไว้ใน [ตั้งค่าคอนฟิกการส่งออกไปยัง Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) ได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="f130b-161">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="f130b-162">ถ้าคุณต้องการดำเนินการตั้งค่าด้วยตนเอง ให้ข้ามกระบวนงานนี้ และดำเนินการต่อด้วยกระบวนงานในส่วน [การตั้งค่าด้วยตนเอง](#manual-setup)</span><span class="sxs-lookup"><span data-stu-id="f130b-162">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="f130b-163">ทำตามขั้นตอนด้านล่างเพื่อรันสคริปต์ PowerShell</span><span class="sxs-lookup"><span data-stu-id="f130b-163">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="f130b-164">ตัวเลือก Azure CLI "ลอง" หรือการรันสคริปต์บนพีซีของคุณ อาจไม่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="f130b-164">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="f130b-165">ทำตามขั้นตอนต่อไปนี้เพื่อตั้งค่าคอนฟิก Azure โดยใช้สคริปต์ Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f130b-165">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="f130b-166">คุณต้องมีสิทธิ์ในการสร้างกลุ่มทรัพยากร Azure ทรัพยากร Azure และแอปพลิเคชัน Azure AD</span><span class="sxs-lookup"><span data-stu-id="f130b-166">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="f130b-167">สำหรับข้อมูลเกี่ยวกับสิทธิ์ที่จำเป็น ให้ดูที่ [ตรวจสอบสิทธิ์ Azure AD](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app)</span><span class="sxs-lookup"><span data-stu-id="f130b-167">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="f130b-168">ใน [พอร์ทัล azure](https://portal.azure.com) ให้ไปที่การบอกรับเป็นสมาชิก Azure เป้าหมายของคุณ</span><span class="sxs-lookup"><span data-stu-id="f130b-168">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="f130b-169">เลือกปุ่ม **Cloud Shell** ทางด้านขวาของฟิลด์ **ค้นหา**</span><span class="sxs-lookup"><span data-stu-id="f130b-169">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="f130b-170">เลือก **PowerShell**</span><span class="sxs-lookup"><span data-stu-id="f130b-170">Select **PowerShell**.</span></span>
3. <span data-ttu-id="f130b-171">สร้างที่เก็บข้อมูล ถ้าคุณได้รับพร้อมท์ให้ดำเนินการดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="f130b-171">Create storage, if you're prompted to do so.</span></span> <span data-ttu-id="f130b-172">จากนั้น อัปโหลดสคริปต์ Windows PowerShell ไปที่รอบเวลา</span><span class="sxs-lookup"><span data-stu-id="f130b-172">Then upload the Windows PowerShell script to the session.</span></span>
4. <span data-ttu-id="f130b-173">รันสคริปต์</span><span class="sxs-lookup"><span data-stu-id="f130b-173">Run the script.</span></span>
5. <span data-ttu-id="f130b-174">ติดตามพร้อมท์เพื่อรันสคริปต์</span><span class="sxs-lookup"><span data-stu-id="f130b-174">Follow the prompts to run the script.</span></span>
6. <span data-ttu-id="f130b-175">ใช้ข้อมูลจากเอาต์พุตของสคริปต์เพื่อติดตั้ง add-in **ส่งออกไปยัง Data Lake** ใน LCS</span><span class="sxs-lookup"><span data-stu-id="f130b-175">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
7. <span data-ttu-id="f130b-176">ใช้ข้อมูลจากเอาต์พุตของสคริปต์เพื่อเปิดใช้งานที่จัดเก็บเอนทิตีบนหน้า **การเชื่อมต่อข้อมูล** ใน Finance (**การจัดการระบบ \> พารามิเตอร์ระบบ \> การเชื่อมต่อข้อมูล**)</span><span class="sxs-lookup"><span data-stu-id="f130b-176">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="f130b-177">การตั้งค่าด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="f130b-177">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="f130b-178">เพิ่มแอปพลิเคชันในผู้เช่า Azure AD</span><span class="sxs-lookup"><span data-stu-id="f130b-178">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="f130b-179">ใน [พอร์ทัล Azure](https://portal.azure.com) ไปยัง **Azure Active Directory**</span><span class="sxs-lookup"><span data-stu-id="f130b-179">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="f130b-180">เลือก **จัดการ \> แอปพลิเคชันองค์กร**</span><span class="sxs-lookup"><span data-stu-id="f130b-180">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="f130b-181">ค้นหาแอปพลิเคชันต่อไปนี้ตามรหัสของแอป</span><span class="sxs-lookup"><span data-stu-id="f130b-181">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="f130b-182">ใบคำขอเปิด</span><span class="sxs-lookup"><span data-stu-id="f130b-182">Application</span></span>                              | <span data-ttu-id="f130b-183">รหัสแอพ</span><span class="sxs-lookup"><span data-stu-id="f130b-183">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="f130b-184">Microsoft Dynamics ERP Microservices</span><span class="sxs-lookup"><span data-stu-id="f130b-184">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="f130b-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="f130b-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="f130b-186">Microsoft Dynamics ERP Microservices CDS</span><span class="sxs-lookup"><span data-stu-id="f130b-186">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="f130b-187">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="f130b-187">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="f130b-188">บริการตรวจสอบ AI Builder</span><span class="sxs-lookup"><span data-stu-id="f130b-188">AI Builder Authorization Service</span></span>         | <span data-ttu-id="f130b-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="f130b-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="f130b-190">ถ้าคุณไม่พบแอปพลิเคชันก่อนหน้าใดๆ ให้ลองทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f130b-190">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="f130b-191">บนเครื่องเฉพาะที่ของคุณ ให้เลือกเมนู **เริ่มต้น** และค้นหา **powershell**</span><span class="sxs-lookup"><span data-stu-id="f130b-191">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="f130b-192">เลือกและกดค้างไว้ (หรือคลิกขวา) **Windows PowerShell** และจากนั้น เลือก **เรียกใช้ในฐานะผู้ดูแลระบบ**</span><span class="sxs-lookup"><span data-stu-id="f130b-192">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="f130b-193">รันคำสั่งต่อไปนี้เพื่อติดตั้งโมดูล **AzureAD**</span><span class="sxs-lookup"><span data-stu-id="f130b-193">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="f130b-194">ถ้าต้องการให้ผู้ให้บริการ NuGet ดำเนินการต่อ ให้เลือก **Y** เพื่อติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="f130b-194">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="f130b-195">ถ้ามีข้อความ "ที่เก็บที่ไม่น่าเชื่อถือ" ปรากฏขึ้น ให้เลือก **Y** เพื่อดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="f130b-195">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="f130b-196">สำหรับแต่ละแอปพลิเคชันที่ต้องมีการเพิ่ม ให้รันคำสั่งต่อไปนี้เพื่อเพิ่มแอปพลิเคชันไปยัง Azure AD</span><span class="sxs-lookup"><span data-stu-id="f130b-196">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="f130b-197">เมื่อคุณได้รับพร้อมท์ ให้ลงชื่อเข้าใช้ในฐานะผู้ดูแลระบบ Azure AD</span><span class="sxs-lookup"><span data-stu-id="f130b-197">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="f130b-198">สร้างแหล่งข้อมูล Azure</span><span class="sxs-lookup"><span data-stu-id="f130b-198">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="f130b-199">ตรวจสอบให้แน่ใจว่าคุณได้สร้างทรัพยากรต่อไปนี้ในอินสแตนซ์ Azure AD ที่เหมือนกันกับสภาพแวดล้อม Dataverse</span><span class="sxs-lookup"><span data-stu-id="f130b-199">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="f130b-200">คุณไม่สามารถใช้ทรัพยากรจากอินสแตนซ์ Azure AD อื่นได้</span><span class="sxs-lookup"><span data-stu-id="f130b-200">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="f130b-201">การสร้างบัญชีที่จัดเก็บใหม่:</span><span class="sxs-lookup"><span data-stu-id="f130b-201">Create a new storage account:</span></span>

    1. <span data-ttu-id="f130b-202">ใน [พอร์ทัล Azure](https://portal.azure.com) ให้สร้างบัญชีที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="f130b-202">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="f130b-203">ในกล่องโต้ตอบ **สร้างบัญชีที่จัดเก็บ** ให้ตั้งค่าฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f130b-203">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="f130b-204">**สถานที่** – เลือกศูนย์ข้อมูลที่เป็นที่ตั้งของสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="f130b-204">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="f130b-205">**ประสิทธิภาพ** – เราขอแนะนำให้คุณเลือก **มาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="f130b-205">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="f130b-206">**ชนิดบัญชี** – คุณต้องเลือก **StorageV2**</span><span class="sxs-lookup"><span data-stu-id="f130b-206">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="f130b-207">ในกล่องโต้ตอบ **ตัวเลือกขั้นสูง** สำหรับตัวเลือก **Data Lake storage Gen2** เลือก **เปิดใช้งาน** ภายใต้คุณลักษณะ **namespaces ตามลำดับชั้น**</span><span class="sxs-lookup"><span data-stu-id="f130b-207">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="f130b-208">ถ้าคุณปิดใช้งานคุณลักษณะนี้ คุณไม่สามารถใช้ข้อมูลที่แอป Finance and Operations เขียนโดยใช้บริการต่างๆ เช่น โฟลว์ข้อมูล Power BI</span><span class="sxs-lookup"><span data-stu-id="f130b-208">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="f130b-209">เลือก **รีวิวและสร้าง**</span><span class="sxs-lookup"><span data-stu-id="f130b-209">Select **Review and create**.</span></span> <span data-ttu-id="f130b-210">เมื่อการปรับใช้งานเสร็จสมบูรณ์ จะมีการแสดงทรัพยากรใหม่ในพอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="f130b-210">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="f130b-211">ไปที่บัญชีจัดเก็บข้อมูลที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f130b-211">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="f130b-212">บนเมนูด้านซ้าย ให้เลือก **คีย์การเข้าถึง**</span><span class="sxs-lookup"><span data-stu-id="f130b-212">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="f130b-213">คัดลอกและบันทึกสตริงการเชื่อมต่อสำหรับ **คีย์1** หรือ **คีย์2** อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f130b-213">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="f130b-214">คัดลอกและบันทึกชื่อบัญชีที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="f130b-214">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="f130b-215">สร้าง Key Vault ใหม่:</span><span class="sxs-lookup"><span data-stu-id="f130b-215">Create a new key vault:</span></span>

    1. <span data-ttu-id="f130b-216">ใน [พอร์ทัล Azure](https://portal.azure.com) ให้สร้าง Key Vault</span><span class="sxs-lookup"><span data-stu-id="f130b-216">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="f130b-217">ในกล่องโต้ตอบ **สร้าง Key Vault** ในฟิลด์ **สถานที่** ให้เลือกศูนย์ข้อมูลที่เป็นที่ตั้งของสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="f130b-217">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="f130b-218">หลังจากที่มีการสร้าง Key Vault แล้ว ให้เลือกในรายการ แล้วจากนั้น เลือก **ข้อมูลลับ**</span><span class="sxs-lookup"><span data-stu-id="f130b-218">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="f130b-219">เลือก **สร้าง/นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="f130b-219">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="f130b-220">ในกล่องโต้ตอบ **สร้างข้อมูลลับ** ในฟิลด์ **ตัวเลือกการอัปโหลด** ให้เลือก **ด้วยตนเอง**</span><span class="sxs-lookup"><span data-stu-id="f130b-220">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="f130b-221">ป้อนชื่อสำหรับข้อมูลลับ</span><span class="sxs-lookup"><span data-stu-id="f130b-221">Enter a name for the secret.</span></span> <span data-ttu-id="f130b-222">ให้จดบันทึกชื่อ เนื่องจากคุณจะต้องระบุชื่อนี้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="f130b-222">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="f130b-223">ในฟิลด์ **ค่า** ให้ป้อนสตริงการเชื่อมต่อที่คุณได้รับจากบัญชีที่จัดเก็บในกระบวนงานก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="f130b-223">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="f130b-224">เลือก **เปิดใช้งานแล้ว** แล้วจากนั้น เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="f130b-224">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="f130b-225">ข้อมูลลับจะถูกสร้างขึ้นและเพิ่มเข้าไปใน Key Vault</span><span class="sxs-lookup"><span data-stu-id="f130b-225">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="f130b-226">ไปที่ **ภาพรวมของ Key Vault** และจดบันทึกชื่อของ DNS</span><span class="sxs-lookup"><span data-stu-id="f130b-226">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="f130b-227">สร้างและลงทะเบียนแอปพลิเคชัน Azure AD:</span><span class="sxs-lookup"><span data-stu-id="f130b-227">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="f130b-228">ใน [พอร์ทัล Azure](https://portal.azure.com) ไปยัง **Azure Active Directory** แล้วจากนั้น เลือก **การลงทะเบียนแอป**</span><span class="sxs-lookup"><span data-stu-id="f130b-228">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="f130b-229">เลือก **การลงทะเบียนแอปพลิเคชันใหม่** และตั้งค่าฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f130b-229">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="f130b-230">**ชื่อ** – ป้อนชื่อของแอป</span><span class="sxs-lookup"><span data-stu-id="f130b-230">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="f130b-231">**ชนิดของแอปพลิเคชัน** – เลือก **Web API**</span><span class="sxs-lookup"><span data-stu-id="f130b-231">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="f130b-232">**เปลี่ยนเส้นทางการตั้งค่า URI** – ป้อน URL สำหรับอินสแตนซ์ Dynamics 365 ของคุณ เช่น `https://yourdynamicsinstance.dynamics.com/auth`</span><span class="sxs-lookup"><span data-stu-id="f130b-232">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="f130b-233">ไปที่แอปพลิเคชันที่คุณเพิ่งสร้างขึ้น และคัดลอกและบันทึกค่า **รหัสของแอปพลิเคชัน (ไคลเอนต์)**</span><span class="sxs-lookup"><span data-stu-id="f130b-233">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="f130b-234">คุณจะต้องระบุค่านี้ในภายหลัง เมื่อคุณตั้งค่า key vault</span><span class="sxs-lookup"><span data-stu-id="f130b-234">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="f130b-235">ไปที่ **สิทธิ์ของ API** และปฏิบัติตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="f130b-235">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="f130b-236">เลือก **เพิ่มสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="f130b-236">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="f130b-237">เลือก **Azure Key Vault**</span><span class="sxs-lookup"><span data-stu-id="f130b-237">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="f130b-238">หลังจากที่คุณเลือกสิทธิ์ที่ได้รับมอบหมาย ให้เลือก **ผู้ใช้\_การเลียนแบบ**</span><span class="sxs-lookup"><span data-stu-id="f130b-238">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="f130b-239">เลือก **เพิ่มสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="f130b-239">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="f130b-240">บนเมนูสำหรับแอป ให้เลือก **ใบรับรอง \& ข้อมูลลับ** และจากนั้น ทำตามขั้นตอนต่อไปนี้เพื่อสร้างข้อมูลลับของ Key Vault:</span><span class="sxs-lookup"><span data-stu-id="f130b-240">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="f130b-241">เลือก **ข้อมูลลับของไคลเอนต์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="f130b-241">Select **New client secret**.</span></span>
        2. <span data-ttu-id="f130b-242">ในฟิลด์ **คำอธิบาย Key** ให้ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="f130b-242">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="f130b-243">เลือกระยะเวลา แล้วจากนั้น เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="f130b-243">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="f130b-244">ข้อมูลลับจะถูกสร้างขึ้นในฟิลด์ **ค่า**</span><span class="sxs-lookup"><span data-stu-id="f130b-244">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="f130b-245">คัดลอกและบันทึกค่าลับ</span><span class="sxs-lookup"><span data-stu-id="f130b-245">Copy and save the secret value.</span></span>

4. <span data-ttu-id="f130b-246">สร้างข้อมูลลับของ Key Vault:</span><span class="sxs-lookup"><span data-stu-id="f130b-246">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="f130b-247">ไปที่ Key Vault ที่คุณสร้างไว้ก่อนหน้านี้ และเลือก **ข้อมูลลับ**</span><span class="sxs-lookup"><span data-stu-id="f130b-247">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="f130b-248">สำหรับชื่อลับแต่ละชื่อในตารางต่อไปนี้ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="f130b-248">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="f130b-249">เลือก **สร้าง/นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="f130b-249">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="f130b-250">ในกล่องโต้ตอบ **สร้างข้อมูลลับ** ในฟิลด์ **ตัวเลือกการอัปโหลด** ให้เลือก **ด้วยตนเอง**</span><span class="sxs-lookup"><span data-stu-id="f130b-250">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="f130b-251">สร้างชื่อและค่าลับจากตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f130b-251">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="f130b-252">เลือก **เปิดใช้งานแล้ว** แล้วจากนั้น เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="f130b-252">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="f130b-253">ข้อมูลลับจะถูกสร้างขึ้นและเพิ่มเข้าไปใน Key Vault</span><span class="sxs-lookup"><span data-stu-id="f130b-253">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="f130b-254">ชื่อข้อมูลลับ</span><span class="sxs-lookup"><span data-stu-id="f130b-254">Secret name</span></span>                       | <span data-ttu-id="f130b-255">ค่าลับ</span><span class="sxs-lookup"><span data-stu-id="f130b-255">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="f130b-256">รหัสแอป</span><span class="sxs-lookup"><span data-stu-id="f130b-256">app-id</span></span>                            | <span data-ttu-id="f130b-257">รหัสแอปของแอปพลิเคชันที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="f130b-257">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="f130b-258">ข้อมูลลับของแอป</span><span class="sxs-lookup"><span data-stu-id="f130b-258">app-secret</span></span>                        | <span data-ttu-id="f130b-259">ความลับของไคลเอนต์ที่คุณบันทึกไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="f130b-259">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="f130b-260">ชื่อบัญชีที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="f130b-260">storage-account-name</span></span>              | <span data-ttu-id="f130b-261">ชื่อของบัญชีที่จัดเก็บที่คุณสร้างไว้ก่อนหน้านี้ เช่น **storageaccount1**</span><span class="sxs-lookup"><span data-stu-id="f130b-261">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="f130b-262">สตริง-การเชื่อมต่อ-บัญชี-ที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="f130b-262">storage-account-connection-string</span></span> | <span data-ttu-id="f130b-263">สตริงการเชื่อมต่อที่คุณคัดลอกมาจากหน้า **คีย์การเข้าถึง** สำหรับบัญชีที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="f130b-263">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="f130b-264">อนุญาตให้แอปพลิเคชันเข้าถึง key vault:</span><span class="sxs-lookup"><span data-stu-id="f130b-264">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="f130b-265">ใน [พอร์ทัล Azure](https://portal.azure.com) ให้เปิด key vault ที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="f130b-265">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="f130b-266">เลือกนโยบายการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="f130b-266">Select the access policies.</span></span>
    3. <span data-ttu-id="f130b-267">สำหรับแต่ละแอปพลิเคชันในตารางต่อไปนี้ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="f130b-267">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="f130b-268">เลือก **เพิ่มนโยบายการเข้าถึง** เพื่อสร้างนโยบายการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="f130b-268">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="f130b-269">ในฟิลด์ **สิทธิ์ของข้อมูลลับ** ให้เลือกสิทธิ์จากตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f130b-269">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="f130b-270">ในฟิลด์ **หลักการเลือก** ให้ค้นหาชื่อที่แสดงของแอปพลิเคชันจากตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f130b-270">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="f130b-271">เลือก **เลือก**</span><span class="sxs-lookup"><span data-stu-id="f130b-271">Select **Select**.</span></span>
        5. <span data-ttu-id="f130b-272">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="f130b-272">Select **Add**.</span></span>
        6. <span data-ttu-id="f130b-273">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f130b-273">Select **Save**.</span></span>

        | <span data-ttu-id="f130b-274">ใบคำขอเปิด</span><span class="sxs-lookup"><span data-stu-id="f130b-274">Application</span></span>                                              | <span data-ttu-id="f130b-275">สิทธิ์</span><span class="sxs-lookup"><span data-stu-id="f130b-275">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="f130b-276">ชื่อที่แสดงของแอปพลิเคชันใหม่ที่คุณสร้าง</span><span class="sxs-lookup"><span data-stu-id="f130b-276">The display name of the new application that you created</span></span> | <span data-ttu-id="f130b-277">เรียกดู รายการ</span><span class="sxs-lookup"><span data-stu-id="f130b-277">Get, List</span></span>   |
        | <span data-ttu-id="f130b-278">**Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="f130b-278">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="f130b-279">เรียกดู รายการ</span><span class="sxs-lookup"><span data-stu-id="f130b-279">Get, List</span></span>   |

6. <span data-ttu-id="f130b-280">กำหนดบทบาทที่จะเข้าถึงบัญชีที่จัดเก็บ:</span><span class="sxs-lookup"><span data-stu-id="f130b-280">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="f130b-281">ใน [พอร์ทัล Azure](https://portal.azure.com) ให้เปิดบัญชีที่จัดเก็บที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="f130b-281">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="f130b-282">เลือก **การควบคุมการเข้าถึง (IAM)** และจากนั้น เลือก **การกำหนดบทบาท**</span><span class="sxs-lookup"><span data-stu-id="f130b-282">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="f130b-283">เลือก **เพิ่ม เพิ่มการกำหนดบทบาท**</span><span class="sxs-lookup"><span data-stu-id="f130b-283">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="f130b-284">สำหรับแต่ละแอปพลิเคชันในตารางต่อไปนี้ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="f130b-284">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="f130b-285">เลือกบทบาทจากตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f130b-285">Select the role from the following table.</span></span>
        2. <span data-ttu-id="f130b-286">ปล่อยฟิลด์ **กำหนดการเข้าถึงแก่** ให้มีการตั้งค่าเป็น **ผู้ใช้ กลุ่ม หรือผู้ใช้งานบริการ Azure AD**</span><span class="sxs-lookup"><span data-stu-id="f130b-286">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="f130b-287">ในฟิลด์ **เลือก** ให้ป้อนแอปพลิเคชันจากตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f130b-287">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="f130b-288">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f130b-288">Select **Save**.</span></span>

        | <span data-ttu-id="f130b-289">ใบคำขอเปิด</span><span class="sxs-lookup"><span data-stu-id="f130b-289">Application</span></span>                                              | <span data-ttu-id="f130b-290">บทบาท</span><span class="sxs-lookup"><span data-stu-id="f130b-290">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="f130b-291">ชื่อที่แสดงของแอปพลิเคชันใหม่ที่คุณสร้าง</span><span class="sxs-lookup"><span data-stu-id="f130b-291">The display name of the new application that you created</span></span> | <span data-ttu-id="f130b-292">เจ้าของ</span><span class="sxs-lookup"><span data-stu-id="f130b-292">Owner</span></span>                       |
        | <span data-ttu-id="f130b-293">ชื่อที่แสดงของแอปพลิเคชันใหม่ที่คุณสร้าง</span><span class="sxs-lookup"><span data-stu-id="f130b-293">The display name of the new application that you created</span></span> | <span data-ttu-id="f130b-294">ผู้จ่ายสมทบ</span><span class="sxs-lookup"><span data-stu-id="f130b-294">Contributor</span></span>                 |
        | <span data-ttu-id="f130b-295">ชื่อที่แสดงของแอปพลิเคชันใหม่ที่คุณสร้าง</span><span class="sxs-lookup"><span data-stu-id="f130b-295">The display name of the new application that you created</span></span> | <span data-ttu-id="f130b-296">ผู้สนับสนุนบัญชีที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="f130b-296">Storage Account Contributor</span></span> |
        | <span data-ttu-id="f130b-297">ชื่อที่แสดงของแอปพลิเคชันใหม่ที่คุณสร้าง</span><span class="sxs-lookup"><span data-stu-id="f130b-297">The display name of the new application that you created</span></span> | <span data-ttu-id="f130b-298">เจ้าของข้อมูล Blob ที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="f130b-298">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="f130b-299">**บริการตรวจสอบ AI Builder**</span><span class="sxs-lookup"><span data-stu-id="f130b-299">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="f130b-300">ตัวอ่านข้อมูล Blob ที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="f130b-300">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="f130b-301">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="f130b-301">Azure CLI</span></span>](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    Assert-ScriptSetup

    $ClientAppName = 'Finance Data Lake Application'
    $DefaultSecretExpiryInYear = 1
    $MicrosoftDynamicsERPMicroservicesAppId = '0cdb527f-a8d1-4bf8-9436-b352c68682b2'
    $MicrosoftDynamicsERPMicroservicesCDSAppId = '703e2651-d3fc-48f5-942c-74274233dba8'
    $AIBuilderAuthorizationServiceAppId = 'ad40333e-9910-4b61-b281-e3aeeb8c3ef3'
    $KeyVaultServicePrincipalAppId = 'cfa8b339-82a2-471a-a3c9-0fc0be7a4093'
    $GraphServicePrincipalAppId = '00000003-0000-0000-c000-000000000000'

    Import-Module AzureAD.Standard.Preview
    $connectAzureADParameters = @{ 'Identity' = $true; 'TenantId' = $env:ACC_TID }
    $azContext = AzureAD.Standard.Preview\Connect-AzureAD @connectAzureADParameters
    $userContext = ConvertFrom-Json ((az ad signed-in-user show) -join '')
    $user = Get-AzureADUser -Filter ("UserPrincipalName eq '" + $userContext.UserPrincipalName + "'")

    Set-AzureSubscription
    
    $resourceGroup = $null
    $ResourceGroupName = 'D365FinanceInsightsDataLake'
    $ResourceGroupNameSuffix = ''
    $FullResourceGroupName = ''
    Write-Output ("The default Azure Resource Group name is '{0}'" -f $ResourceGroupName)
    while (-not ($resourceGroup)) {
        $ResourceGroupNameSuffix = (Read-Host -Prompt "Enter optional Azure Resource Group name suffix: (leave blank for no suffix)")
        if ([string]::IsNullOrWhitespace($ResourceGroupNameSuffix))
        {
            $FullResourceGroupName = $ResourceGroupName
        }
        else
        {
            if ($ResourceGroupNameSuffix -notmatch "^[A-Za-z0-9]+$") {
                Write-Warning "The Azure Resource Group name suffix can only include alphanumeric characters."
                continue
            }

            if ($ResourceGroupNameSuffix.Length -gt 60) {
                Write-Warning "The Azure Resource Group name suffix cannot be longer than 60 characters."
                continue
            }

            $FullResourceGroupName = $ResourceGroupName + $ResourceGroupNameSuffix
        }
        
        $resourceGroup = Get-AzResourceGroup -Name $FullResourceGroupName -ErrorAction SilentlyContinue

        if (-not ($resourceGroup)) {
            Write-Output ("Your new Azure Resource Group name is '{0}'" -f $FullResourceGroupName)
            $resourceLocation = ''
            $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
            while ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations))) {
                $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
                if ($resourceLocation -eq 'help') {
                    Write-Output ("List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
                elseif ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations)))
                {
                    Write-Warning ("The provided location is not available for resource group. List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
            }
            $resourceGroup = New-AzResourceGroup -Name $FullResourceGroupName -Location $resourceLocation
            Write-Output ("Created Azure Resource Group '{0}'" -f $resourceGroup.ResourceGroupName)
        }
        else {
            Write-Output ("Found Azure Resource Group '{0}'" -f ($resourceGroup.ResourceGroupName))
        }
    }

    Write-Output '================================================================================='
    $MicrosoftDynamicsERPMicroservicesAppObjectId = Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId
    Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Out-Null
    $aibuilderAuthorizationServiceObjectId = Create-ADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId
    Write-Output ('=================================================================================')

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $ClientAppName + "'")
    if (-not ($clientAppSPN)) {
        $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        if (-not $keyVaultPrincipal)
        {
            New-AzureADServicePrincipal -AppId $KeyVaultServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Key Vault principal to AAD"
            $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        }
        $keyVaultAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $keyVaultAccess.ResourceAppId = $keyVaultPrincipal.AppId
        $keyVaultAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $keyVaultPrincipal.Oauth2Permissions.Id, "Scope")

        $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        if (-not $graphPrincipal)
        {
            New-AzureADServicePrincipal -AppId $GraphServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Graph principal to AAD"
            $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        }
        $userRead = $graphPrincipal.Oauth2Permissions | Where-Object { $_.Type -eq "User" -and $_.Value -eq "User.Read" }
        $graphAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $graphAccess.ResourceAppId = $graphPrincipal.AppId
        $graphAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $userRead.Id, "Scope")

        $clientApp = New-AzureADApplication -DisplayName $ClientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($ClientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $ClientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($DefaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    try {
        $deployment = New-AzResourceGroupDeployment -ResourceGroupName $FullResourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId -Force -ErrorAction Stop
    }
    catch {
        $ErrorMessage = $_.Exception.Message
        if ($ErrorMessage.Contains("not allowed to be updated"))
        {
            Write-Error ($ErrorMessage)
            Write-Warning "Some items in the existing resource group $FullResourceGroupName could not be updated. To resolve the issue, remove the existing resource group $FullResourceGroupName and run the script again."
        }
        else {
            throw
        }

    }
    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
        
        $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
        $tenantId = (Get-AzContext).Tenant.Id

        Write-Output "Values for LCS Data Lake Add-In:"
        Write-Output ("  Tenant ID:                         " + $tenantId)
        Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
        Write-Output "  Storage account secret name:       storage-account-name"
        Write-Output "  Application ID secret name:        app-id"
        Write-Output "  Application Secret secret name:    app-secret"
        Write-Warning "Copy this information for the LCS Add-in for easy access. Azure Cloud Shell will eventually time out and close."

        Write-Output '================================================================================='
        Write-Output "Values for System parameters > Data connections:"
        Write-Output ("  Application ID:                    " + $clientAppId)
        Write-Output ("  Application Secret:                " + $ClientAppSecret)
        Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
        Write-Output "  Secret name:                       storage-account-connection-string"
        Write-Warning "Copy this information for the System parameters for easy access. Azure Cloud Shell will eventually time out and close."
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $FullResourceGroupName)
    }
}

function Assert-ScriptSetup {
    if ($PSVersionTable.PSEdition -ne 'Core' -or -not $env:ACC_TID) { 
        throw "This script needs to be uploaded and run from Azure Cloud Shell (PowerShell)." 
    }
    
    if ((Get-AzContext) -eq $null -and (Connect-AzAccount) -eq $null) {
        throw 'Unable to connect to Azure account.'
    }
}

function Set-AzureSubscription {
    $azSubscription = $null
    while (-not ($azSubscription)) {
        $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (leave blank for default)")
        if ([string]::IsNullOrWhitespace($subscriptionId)){
            break
        }
        elseif (-not [guid]::TryParse($subscriptionId, $([ref][guid]::Empty))) {
                Write-Warning "Azure Subscription ID must be a valid GUID."
                continue
        }

        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }
}

function Create-ADServicePrincipal {
    param (
        [string] $AppId
    )

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AppId | Out-Null
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
        Write-Host ("Added AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }
    else {
        Write-Host ("Found AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }

    return $service.ObjectId
}

$azureTemplate = @"
{
    "contentVersion": "1.0.0.0",
    "parameters": {
      "aibuilderAppObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of the AI Builder application."
        }
      },
      "clientAppId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the application ID of client application."
        }
      },
      "clientAppSecret": {
        "type": "String",
        "metadata": {
          "description": "Specifies the Azure App ID client secret to in azure key vault."
        }
      },
      "clientAppSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of a client application service principal."
        }
      },
      "userSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of tenant admin service principal."
        }
      },
      "microserviceSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of Microsoft Dynamics ERP Microservices service principal."
        }
      },
      "storageAccountType": {
        "type": "string",
        "defaultValue": "Standard_LRS",
        "allowedValues": [
          "Standard_LRS",
          "Standard_GRS",
          "Standard_ZRS",
          "Premium_LRS"
        ],
        "metadata": {
          "description": "Storage Account type"
        }
      }
    },
    "variables": {
      "storageAccountApiVersion": "2019-06-01",
      "keyVaultApiVersion": "2018-02-14",
      "secretsPermissions": [
        "list",
        "get"
      ],
      "location": "[resourceGroup().location]",
      "storageAccountName": "[concat('store', uniquestring(resourceGroup().id))]",
      "keyVaultName": "[concat('keyvault', uniquestring(resourceGroup().id))]",
      "owner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '8e3af657-a8ff-443c-a75c-2fe8c4bcb635')]",
      "contributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b24988ac-6180-42a0-ab88-20f7382dd24c')]",
      "storageAccountContributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '17d1049b-9a84-46fb-8f53-869881c3d3ab')]",
      "storageBlobDataOwner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b7e6dc6d-f1e8-4753-8033-0f276bb0955b')]",
      "storageBlobDataReader": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '2a2b9908-6ea1-4ae2-8e65-a410df84e7d1')]"
    },
    "resources": [
      {
        "type": "Microsoft.Storage/storageAccounts",
        "apiVersion": "[variables('storageAccountApiVersion')]",
        "name": "[variables('storageAccountName')]",
        "location": "[variables('location')]",
        "sku": {
          "name": "[parameters('storageAccountType')]"
        },
        "kind": "StorageV2",
        "properties": {
          "accessTier": "Hot",
          "supportsHttpsTrafficOnly": true,
          "isHnsEnabled": true
        },
        "resources": [
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'1')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('owner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'2')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('contributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'3')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageAccountContributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'4')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataOwner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'5')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataReader')]",
              "principalId": "[parameters('aibuilderAppObjectId')]"
            }
          }
        ]
      },
      {
        "type": "Microsoft.KeyVault/vaults",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "name": "[variables('keyVaultName')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName'))]"
        ],
        "tags": {
        },
        "properties": {
          "enabledForDeployment": false,
          "enabledForTemplateDeployment": false,
          "enabledForDiskEncryption": false,
          "enableRbacAuthorization": false,
          "accessPolicies": [
            {
              "objectId": "[parameters('clientAppSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('microserviceSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('userSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            }
          ],
          "tenantId": "[subscription().tenantId]",
          "sku": {
            "name": "Standard",
            "family": "A"
          },
          "enableSoftDelete": false,
          "networkAcls": {
            "defaultAction": "Allow",
            "bypass": "AzureServices"
          }
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-id')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppId')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-secret')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppSecret')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-name')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[variables('storageAccountName')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-connection-string')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[concat('DefaultEndpointsProtocol=https;AccountName=', variables('storageAccountName'), ';AccountKey=', listKeys(resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName')), variables('storageAccountApiVersion')).keys[0].value, ';EndpointSuffix=core.windows.net')]"
        }
      }
    ],
    "outputs": {
      "storageAccountName": {
        "type": "string",
        "value": "[variables('storageAccountName')]"
      },
      "keyVaultName": {
        "type": "string",
        "value": "[variables('keyVaultName')]"
      }
    }
  }
"@

try {
  Start-Transcript -path (Join-Path $HOME Provision-FinInsights-Azure.log)
  New-FinanceDataLakeAzureResources
}
catch {
  Write-Error $_.Exception.Message

  if ($PSItem.Exception.StackTrace -ne $null)
  {
      Write-Warning $_.Exception.StackTrace
  }

  $inner = $_.Exception.InnerException
  while ($null -ne $inner) {
    Write-Output 'Inner Exception:'
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $inner.InnerException
  }
}
finally {
  Stop-Transcript
}

```
---



## <a name="configure-the-data-lake"></a><span data-ttu-id="f130b-302">ตั้งค่าคอนฟิก data lake</span><span class="sxs-lookup"><span data-stu-id="f130b-302">Configure the data lake</span></span>

<span data-ttu-id="f130b-303">ทำตามขั้นตอนต่อไปนี้เพื่อใช้ LCS เพื่อเพิ่ม add-in ของ Azure Data Lake ไปยังสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="f130b-303">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="f130b-304">ลงชื่อเข้าใช้ LCS แล้วจากนั้นภายใต้ชื่อสภาพแวดล้อมทางด้านขวาของหน้า ให้เลือก **รายละเอียดทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="f130b-304">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="f130b-305">ในส่วน **add-in สภาพแวดล้อม** ให้เลือก **ติดตั้ง add-in ใหม่**</span><span class="sxs-lookup"><span data-stu-id="f130b-305">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="f130b-306">เลือก add-in **ส่งออกไปยัง Data Lake**</span><span class="sxs-lookup"><span data-stu-id="f130b-306">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="f130b-307">ป้อนค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f130b-307">Enter the following values.</span></span>

    | <span data-ttu-id="f130b-308">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="f130b-308">Value</span></span>                                                              | <span data-ttu-id="f130b-309">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="f130b-309">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="f130b-310">รหัสผู้เช่าของการบอกรับเป็นสมาชิก Azure ที่เป็นที่ตั้งของ Key Vault</span><span class="sxs-lookup"><span data-stu-id="f130b-310">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="f130b-311">รหัสผู้เช่าซึ่งเป็นที่ตั้งของบัญชีที่จัดเก็บ แอป และ Key Vault</span><span class="sxs-lookup"><span data-stu-id="f130b-311">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="f130b-312">เมื่อต้องการค้นหาค่านี้ ให้เปิด [พอร์ทัล Azure](https://portal.azure.com) ไปที่ **Azure Active Directory** และคัดลอกค่า **รหัสผู้เช่า**</span><span class="sxs-lookup"><span data-stu-id="f130b-312">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="f130b-313">ระบุชื่อ DNS ของ Key Vault ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f130b-313">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="f130b-314">ชื่อ DNS ของ Key Vault เช่น `https://customkeyvault.vault.azure.net/`</span><span class="sxs-lookup"><span data-stu-id="f130b-314">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="f130b-315">(ค่านี้จะตรงกับชื่อ DNS ที่ใช้ในที่จัดเก็บเอนทิตี)</span><span class="sxs-lookup"><span data-stu-id="f130b-315">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="f130b-316">ระบุข้อมูลลับที่มีชื่อของบัญชีที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="f130b-316">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="f130b-317">**ชื่อ-บัญชี-ที่จัดเก็บ**</span><span class="sxs-lookup"><span data-stu-id="f130b-317">**storage-account-name**</span></span> |
    | <span data-ttu-id="f130b-318">ชื่อลับสำหรับรหัสแอปที่จะใช้สำหรับการเข้าถึง Data Lake</span><span class="sxs-lookup"><span data-stu-id="f130b-318">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="f130b-319">**รหัส-แอป**</span><span class="sxs-lookup"><span data-stu-id="f130b-319">**app-id**</span></span> |
    | <span data-ttu-id="f130b-320">ชื่อลับที่จะใช้กับรหัสแอป</span><span class="sxs-lookup"><span data-stu-id="f130b-320">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="f130b-321">**ข้อมูลลับ-แอป**</span><span class="sxs-lookup"><span data-stu-id="f130b-321">**app-secret**</span></span> |

5. <span data-ttu-id="f130b-322">ยอมรับเงื่อนไข และเลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="f130b-322">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="f130b-323">จะมีการติดตั้ง add-in ภายในสองสามนาที</span><span class="sxs-lookup"><span data-stu-id="f130b-323">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="f130b-324">ตั้งค่าคอนฟิก AI Builder</span><span class="sxs-lookup"><span data-stu-id="f130b-324">Configure AI Builder</span></span>

1. <span data-ttu-id="f130b-325">ลงชื่อเข้าใช้ LCS และเปิดหน้า **รายละเอียดสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="f130b-325">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="f130b-326">เลื่อนลงไปที่ส่วน **Add-in ของสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="f130b-326">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="f130b-327">คุณควรเห็น add-in ที่ติดตั้งอยู่แล้วในสภาพแวดล้อมนี้</span><span class="sxs-lookup"><span data-stu-id="f130b-327">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="f130b-328">ถ้า add-in **ส่งออกไปยัง Data Lake** ไม่ได้อยู่ในนั้น ตั้งค่าคอนฟิก add-in นี้</span><span class="sxs-lookup"><span data-stu-id="f130b-328">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="f130b-329">เลือก add-in **รับข้อมูลเชิงลึก**</span><span class="sxs-lookup"><span data-stu-id="f130b-329">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="f130b-330">บนหน้ารายละเอียด add-in  **รับข้อมูลเชิงลึก** ให้ป้อนค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f130b-330">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="f130b-331">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="f130b-331">Value</span></span>                                                    | <span data-ttu-id="f130b-332">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="f130b-332">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="f130b-333">URL ขององค์กร CDS</span><span class="sxs-lookup"><span data-stu-id="f130b-333">CDS Organization URL</span></span>                                     | <span data-ttu-id="f130b-334">URL ขององค์กร Dataverse ของอินสแตนซ์ Dataverse</span><span class="sxs-lookup"><span data-stu-id="f130b-334">The Dataverse organization URL of the Dataverse instance.</span></span> <span data-ttu-id="f130b-335">เมื่อต้องการค้นหาค่านี้ ให้เปิด [พอร์ทัล Power Apps](https://make.powerapps.com) เลือกปุ่ม **การตั้งค่า** (สัญลักษณ์เกียร์) ที่มุมบนขวา ให้เลือก **การตั้งค่าขั้นสูง** และคัดลอก URL</span><span class="sxs-lookup"><span data-stu-id="f130b-335">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Advanced settings**, and copy the URL.</span></span> <span data-ttu-id="f130b-336">(URL ลงท้ายด้วย "dynamics.com")</span><span class="sxs-lookup"><span data-stu-id="f130b-336">(The URL ends with "dynamics.com.")</span></span> |
    | <span data-ttu-id="f130b-337">รหัสองค์กร CDS</span><span class="sxs-lookup"><span data-stu-id="f130b-337">CDS Org ID</span></span>                                               | <span data-ttu-id="f130b-338">รหัสสภาพแวดล้อมของอินสแตนซ์ Dataverse</span><span class="sxs-lookup"><span data-stu-id="f130b-338">The environment ID of the Dataverse instance.</span></span> <span data-ttu-id="f130b-339">เมื่อต้องการค้นหาค่านี้ ให้เปิด [พอร์ทัล Power Apps](https://make.powerapps.com) เลือกปุ่ม **การตั้งค่า** (สัญลักษณ์เกียร์) ที่มุมบนขวา ให้เลือก **การเลือกกำหนด \> ทรัพยากรนักพัฒนา \> ข้อมูลอ้างอิงของอินสแตนซ์** และคัดลอกค่า **รหัส**</span><span class="sxs-lookup"><span data-stu-id="f130b-339">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Customizations \> Developer resources \> Instance Reference Information**, and copy the **ID** value.</span></span> |
    | <span data-ttu-id="f130b-340">รหัสผู้เช่าของ CDS (รหัสไดเรกทอรีจาก AAD)</span><span class="sxs-lookup"><span data-stu-id="f130b-340">CDS Tenant ID (Directory ID from AAD)</span></span>               | <span data-ttu-id="f130b-341">รหัสผู้เช่าของอินสแตนซ์ Dataverse</span><span class="sxs-lookup"><span data-stu-id="f130b-341">The tenant ID of the Dataverse instance.</span></span> <span data-ttu-id="f130b-342">เมื่อต้องการค้นหาค่านี้ ให้เปิด [พอร์ทัล Azure](https://portal.azure.com) ไปที่ **Azure Active Directory** และคัดลอกค่า **รหัสผู้เช่า**</span><span class="sxs-lookup"><span data-stu-id="f130b-342">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="f130b-343">ระบุรหัสออบเจ็กต์ผู้ใช้ที่มีบทบาทผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="f130b-343">Provide user object ID who has system administrator role</span></span> | <span data-ttu-id="f130b-344">รหัสออบเจ็กต์ผู้ใช้ Azure AD ของผู้ใช้ใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="f130b-344">The Azure AD user object ID of the user in Dataverse.</span></span> <span data-ttu-id="f130b-345">ผู้ใช้นี้ต้องเป็นผู้ดูแลระบบของอินสแตนซ์ Dataverse</span><span class="sxs-lookup"><span data-stu-id="f130b-345">This user must be a system administrator of the Dataverse instance.</span></span> <span data-ttu-id="f130b-346">เมื่อต้องการค้นหาค่านี้ ให้เปิด [พอร์ทัล Azure](https://portal.azure.com) ไปที่ **Azure Active Directory \> ผู้ใช้** เลือกผู้ใช้ และจากนั้น ในส่วน **รหัสประจำตัว** ให้คัดลอกค่า **รหัสออบเจ็กต์**</span><span class="sxs-lookup"><span data-stu-id="f130b-346">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory \> Users**, select the user, and then, in the **Identity** section, copy the **Object ID** value.</span></span> |
    | <span data-ttu-id="f130b-347">นี่เป็นสภาพแวดล้อม CDS เริ่มต้นสำหรับผู้เช่าหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f130b-347">Is this the default CDS environment for the tenant?</span></span>      | <span data-ttu-id="f130b-348">ถ้าอินสแตนซ์ Dataverse เป็นอินสแตนซ์การผลิตแรกที่สร้างขึ้น ให้เลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="f130b-348">If the Dataverse instance was the first production instance that was created, select this check box.</span></span> <span data-ttu-id="f130b-349">ถ้ามีการสร้างอินสแตนซ์ Dataverse ด้วยตนเอง ให้ยกเลิกการเลือกกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="f130b-349">If the Dataverse instance was manually created, clear this check box.</span></span> |

## <a name="configure-the-entity-store"></a><span data-ttu-id="f130b-350">ตั้งค่าคอนฟิกที่จัดเก็บเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="f130b-350">Configure the entity store</span></span>

<span data-ttu-id="f130b-351">ทำตามขั้นตอนต่อไปนี้เพื่อตั้งค่าที่จัดเก็บเอนทิตีในสภาพแวดล้อมทาง Finance ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f130b-351">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="f130b-352">ไปที่ **การจัดการระบบ \> การตั้งค่า \> พารามิเตอร์ระบบ \> การเชื่อมต่อข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="f130b-352">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="f130b-353">ตั้งค่าตัวเลือก **เปิดใช้งานการรวม Data Lake** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="f130b-353">Set the **Enable Data Lake integration** option to **Yes**.</span></span>
3. <span data-ttu-id="f130b-354">ตั้งค่าฟิลด์ Key Vault ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f130b-354">Set the following key vault fields:</span></span>

    - <span data-ttu-id="f130b-355">**รหัสแอปพลิเคชัน (ไคลเอนต์)** – ป้อนรหัสไคลเอนต์ของแอแพลิเคชันที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="f130b-355">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="f130b-356">**ข้อมูลลับของแอปพลิเคชัน** – ป้อนข้อมูลลับที่คุณบันทึกไว้สำหรับแอปพลิเคชันที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="f130b-356">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="f130b-357">**ชื่อ DNS** – คุณสามารถค้นหาชื่อของ Domain Name System (DNS) บนหน้ารายละเอียดของแอปพลิเคชันที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="f130b-357">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="f130b-358">**ชื่อลับ** – ป้อน **สตริง-การเชื่อมต่อ-บัญชี-ที่จัดเก็บ**</span><span class="sxs-lookup"><span data-stu-id="f130b-358">**Secret name** – Enter **storage-account-connection-string**.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="f130b-359">ผลป้อนกลับและการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="f130b-359">Feedback and support</span></span>

<span data-ttu-id="f130b-360">โปรดส่งอีเมล์ถึง [ข้อมูลเชิงลึกของการชำระเงินของลูกค้า (ตัวอย่าง)](mailto:fiap@microsoft.com) หากคุณมีความสนใจในการให้ผลป้อนกลับหรือต้องการความช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="f130b-360">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="f130b-361">ประกาศความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="f130b-361">Privacy notice</span></span>

<span data-ttu-id="f130b-362">การแสดงตัวอย่าง (1) อาจใช้วิธีการที่มีความปลอดภัยและความเป็นส่วนตัวที่น้อยลงกว่าบริการ Dynamics 365 Finance and Operations (2) ไม่ถูกรวมอยู่ในข้อตกลงระดับการให้บริการ (SLA) สำหรับบริการนี้ (3) ไม่ควรถูกใช้เพื่อประมวลผลข้อมูลส่วนบุคคลหรือข้อมูลอื่นที่อยู่ภายใต้ข้อกำหนดการปฏิบัติตามกฎหมายหรือระเบียบข้อบังคับ และ (4) มีการสนับสนุนที่จำกัด</span><span class="sxs-lookup"><span data-stu-id="f130b-362">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
