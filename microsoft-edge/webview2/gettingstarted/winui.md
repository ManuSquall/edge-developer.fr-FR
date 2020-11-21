---
description: Guide de mise en route de WebView2 pour les applications WinUI
title: Mise en route de WebView2 pour les applications WinUI
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, WinUI applications, WinUI, Edge, CoreWebView2, contrôle de navigateur, html Edge, mise en route, mise en route, .NET
ms.openlocfilehash: a1ccffe332f71ee9d53ff267e8cca6bdbda81703
ms.sourcegitcommit: 02c602379537ab3b9d0a355cea7fcf96fdbd8870
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2020
ms.locfileid: "11182720"
---
# <span data-ttu-id="f7503-104">Commencer à utiliser WebView2 dans WinUI 3 (Preview)</span><span class="sxs-lookup"><span data-stu-id="f7503-104">Getting started with WebView2 in WinUI 3 (Preview)</span></span>  

<span data-ttu-id="f7503-105">Dans cet article, vous allez découvrir comment créer votre première application WebView2 et découvrir les principales fonctionnalités de [Présentation de Microsoft Edge WebView2 (Preview)][Webview2Index].</span><span class="sxs-lookup"><span data-stu-id="f7503-105">In this article, learn how to create your first WebView2 app and about the main features of [Introduction to Microsoft Edge WebView2 (Preview)][Webview2Index].</span></span>  <span data-ttu-id="f7503-106">Votre première application WebView2 utilise WinUI3.</span><span class="sxs-lookup"><span data-stu-id="f7503-106">Your first WebView2 app uses WinUI3.</span></span>  <span data-ttu-id="f7503-107">Pour plus d’informations sur les API individuelles, accédez à informations de référence sur les [API][GithubMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="f7503-107">For more information on individual APIs, navigate to [API reference][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  

## <span data-ttu-id="f7503-108">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="f7503-108">Prerequisites</span></span>  

<span data-ttu-id="f7503-109">Vérifiez que vous disposez de la liste des conditions préalables suivantes avant de poursuivre l’article suivant.</span><span class="sxs-lookup"><span data-stu-id="f7503-109">Ensure you install the following list of pre-requisites before proceeding with the following article.</span></span>  

1.  <span data-ttu-id="f7503-110">Windows 10 version 1803 \ (Build 17134 \) ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f7503-110">Windows 10 version 1803 \(build 17134\) or later.</span></span>  <span data-ttu-id="f7503-111">Pour plus d’informations, accédez à [Windows Update: FAQ][MicrosoftSupport12373].</span><span class="sxs-lookup"><span data-stu-id="f7503-111">For more information, navigate to [Windows Update: FAQ][MicrosoftSupport12373].</span></span>  
1.  <span data-ttu-id="f7503-112">[Canal Canaries Microsoft Edge (chrome)][MicrosoftedgeinsiderDownload] sur Windows 10, Windows 8,1 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f7503-112">[Microsoft Edge (Chromium) Canary channel][MicrosoftedgeinsiderDownload] on Windows 10, Windows 8.1, or Windows 7.</span></span>  
1.  <span data-ttu-id="f7503-113">Visual Studio 2019 version 16,9 preview.</span><span class="sxs-lookup"><span data-stu-id="f7503-113">Visual Studio 2019, version 16.9 Preview.</span></span>  <span data-ttu-id="f7503-114">Pour plus d’informations, accédez à la [bibliothèque d’interface utilisateur Windows 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].</span><span class="sxs-lookup"><span data-stu-id="f7503-114">For more information, navigate to [Windows UI Library 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].</span></span>  
    
    <span data-ttu-id="f7503-115">Incluez les charges de travail suivantes lors de l’installation de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f7503-115">Include the following workloads when you install Visual Studio.</span></span>  
    
    *   <span data-ttu-id="f7503-116">Développement de bureau .NET \ (le programme d’installation installe également .NET 5 \)</span><span class="sxs-lookup"><span data-stu-id="f7503-116">.NET Desktop Development \(the installer also installs .NET 5\)</span></span>  
    *   <span data-ttu-id="f7503-117">Développement de plateforme Windows universelle</span><span class="sxs-lookup"><span data-stu-id="f7503-117">Universal Windows Platform development</span></span>  
        
    <span data-ttu-id="f7503-118">Pour créer des applications C++, vous devez également inclure les charges de travail suivantes.</span><span class="sxs-lookup"><span data-stu-id="f7503-118">To build C++ apps, you must also include the following workloads.</span></span>  
    
    *   <span data-ttu-id="f7503-119">Développement de bureau avec C++</span><span class="sxs-lookup"><span data-stu-id="f7503-119">Desktop development with C++</span></span>  
    *   <span data-ttu-id="f7503-120">Les outils de plateforme Windows universelle en C++ (V142) pour la charge de travail de la plateforme Windows universelle.</span><span class="sxs-lookup"><span data-stu-id="f7503-120">The C++ (v142) Universal Windows Platform tools optional component for the Universal Windows Platform workload.</span></span>  <span data-ttu-id="f7503-121">Pour plus d’informations, accédez à détails sur l’installation dans la section développement de plateforme Windows universelle, dans le volet droit.</span><span class="sxs-lookup"><span data-stu-id="f7503-121">For more information,  navigate to Installation Details under the Universal Windows Platform development section, on the right pane.</span></span>  
        
1.  <span data-ttu-id="f7503-122">Assurez-vous que la source du package NuGet est activée sur votre système pour [NuGet.org][NugetHome].  Pour plus d’informations, accédez aux [configurations NuGet communes][NugetConsumePackagesConfiguringNugetBehavior] et au kit de configuration de la [communauté Windows][WindowsCommunitytoolkit].</span><span class="sxs-lookup"><span data-stu-id="f7503-122">Make sure your system has a NuGet package source enabled for [nuget.org][NugetHome].  For more information, navigate to [Common NuGet configurations][NugetConsumePackagesConfiguringNugetBehavior] and [Windows Community Toolkit][WindowsCommunitytoolkit].</span></span>  
1.  <span data-ttu-id="f7503-123">Téléchargez et installez le [package VSIX 3 Preview][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]3.</span><span class="sxs-lookup"><span data-stu-id="f7503-123">Download and install the [WinUI 3 Preview 3 VSIX package][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates].</span></span>  <span data-ttu-id="f7503-124">Le programme d’installation ajoute les modèles de projet WinUI 3 et le package NuGet contenant les bibliothèques WinUI 3 à Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="f7503-124">The installer adds both the WinUI 3 project templates and the NuGet package containing the WinUI 3 libraries to Visual Studio 2019.</span></span>  
    
    <span data-ttu-id="f7503-125">Pour obtenir des instructions sur la façon d’ajouter le package VSIX à Visual Studio, accédez à la section [recherche et utilisation des extensions Visual Studio][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].</span><span class="sxs-lookup"><span data-stu-id="f7503-125">For instructions on how to add the VSIX package to Visual Studio, navigate to [Finding and Using Visual Studio Extensions][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].</span></span>
    
1.  <span data-ttu-id="f7503-126">Activez le [mode développeur][WindowsUwpGetStartedEnableYourDeviceForDevelopment] pour vous assurer que vous avez accès à toutes les fonctionnalités de Visual Studio spécifiques aux développeurs.</span><span class="sxs-lookup"><span data-stu-id="f7503-126">Enable [Developer Mode][WindowsUwpGetStartedEnableYourDeviceForDevelopment] to ensure you have access to all developer-specific Visual Studio features.</span></span>  
    
## <span data-ttu-id="f7503-127">Étape 1: créer un projet</span><span class="sxs-lookup"><span data-stu-id="f7503-127">Step 1 - Create Project</span></span>  

<span data-ttu-id="f7503-128">Utiliser un projet de bureau de base contenant une seule fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="f7503-128">Start with a basic desktop project containing a single main window.</span></span>  

1.  <span data-ttu-id="f7503-129">Dans Visual Studio, sélectionnez **créer un nouveau projet**.</span><span class="sxs-lookup"><span data-stu-id="f7503-129">In Visual Studio, choose **Create a new project**.</span></span>  
1.  <span data-ttu-id="f7503-130">Dans la liste déroulante projet, sélectionnez respectivement **C#**, **Windows**et **WinUI** .</span><span class="sxs-lookup"><span data-stu-id="f7503-130">In the project drop-down, choose **C#**, **Windows**, and **WinUI** respectively.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Créer un projet WinUI à l’aide de Visual Studio" lightbox="./media/winui-gettingstarted-selections.png":::
        <span data-ttu-id="f7503-132">Créer un projet WinUI à l’aide de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f7503-132">Create a new WinUI project using Visual Studio</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="f7503-133">Sélectionnez **application vide, empaquetée (WinUI dans le bureau)**, puis sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="f7503-133">Choose **Blank App, Packaged (WinUI in Desktop)**, and then choose **Next**.</span></span>  
1.  <span data-ttu-id="f7503-134">Entrez le nom d’un projet et sélectionnez les autres options souhaitées, puis cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="f7503-134">Enter a project name, choose other options as needed, and then choose **Create**.</span></span>  
1.  <span data-ttu-id="f7503-135">Dans **nouveau projet de plateforme Windows universelle**, sélectionnez les valeurs suivantes, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7503-135">In **New Universal Windows Platform Project**, choose the following values, and then choose **OK**.</span></span>  
    *   <span data-ttu-id="f7503-136">**Version cible**:  **Windows 10, version 1903 (Build 18362)** ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="f7503-136">**Target version**:  **Windows 10, version 1903 (build 18362)** or later</span></span>  
    *   <span data-ttu-id="f7503-137">**Version minimum**:  **Windows 10, version 1803 (Build 17134)**</span><span class="sxs-lookup"><span data-stu-id="f7503-137">**Minimum version**:  **Windows 10, version 1803 (build 17134)**</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="Nouvelle boîte de dialogue projet de plateforme Windows universelle avec les valeurs choisies pour la version cible et version minimum." lightbox="./media/winui-gettingstarted-projecttype.png":::
       <span data-ttu-id="f7503-139">Nouvelle boîte de dialogue projet de plateforme Windows universelle avec les valeurs choisies pour la version cible et version minimum.</span><span class="sxs-lookup"><span data-stu-id="f7503-139">The New Universal Windows Platform Project dialog with chosen values for Target version and Minimum version.</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="f7503-140">Dans l’Explorateur de solutions, deux projets sont générés.</span><span class="sxs-lookup"><span data-stu-id="f7503-140">In the Solution Explorer, two projects are generated.</span></span>  
    *   <span data-ttu-id="f7503-141">**Nom de votre projet (bureau)**.</span><span class="sxs-lookup"><span data-stu-id="f7503-141">**Your project name (Desktop)**.</span></span>  <span data-ttu-id="f7503-142">Ce projet contient le code de votre application.</span><span class="sxs-lookup"><span data-stu-id="f7503-142">This project contains the code for your app.</span></span>  <span data-ttu-id="f7503-143">**App.Xaml.cs** définit une `Application` classe qui représente votre instance d’application.</span><span class="sxs-lookup"><span data-stu-id="f7503-143">**App.xaml.cs** defines an `Application` class that represents your app instance.</span></span>  <span data-ttu-id="f7503-144">**MainWindow.Xaml.cs** définit une `MainWindow` classe qui représente la fenêtre principale affichée par votre instance d’application.</span><span class="sxs-lookup"><span data-stu-id="f7503-144">**MainWindow.xaml.cs** defines a `MainWindow` class that represents the main window displayed by your app instance.</span></span>  <span data-ttu-id="f7503-145">Ces classes dérivent de types dans l' `Microsoft.UI.Xaml` espace de noms de l’WinUI.</span><span class="sxs-lookup"><span data-stu-id="f7503-145">These classes derive from types in the `Microsoft.UI.Xaml` namespace of WinUI.</span></span>  
    
    *   <span data-ttu-id="f7503-146">**Nom de votre projet (package)**.</span><span class="sxs-lookup"><span data-stu-id="f7503-146">**Your project name (Package)**.</span></span>  <span data-ttu-id="f7503-147">Ce projet est un projet de création de packages d’application Windows configuré pour générer l’application dans un package MSIX à des fins de déploiement.</span><span class="sxs-lookup"><span data-stu-id="f7503-147">This project is a Windows Application Packaging Project that is configured to build the app into an MSIX package for deployment.</span></span>  <span data-ttu-id="f7503-148">Le projet contient le manifeste du package de votre application, et il s’agit du projet de démarrage de votre solution par défaut.</span><span class="sxs-lookup"><span data-stu-id="f7503-148">The project contains the package manifest for your app, and it is the startup project for your solution by default.</span></span>  <span data-ttu-id="f7503-149">Pour plus d’informations, accédez à [configurer votre application de bureau pour MSIX Packaging dans Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] et [référence de schéma de manifeste de package pour Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span><span class="sxs-lookup"><span data-stu-id="f7503-149">For more information, navigate to [Set up your desktop application for MSIX packaging in Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] and [Package manifest schema reference for Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span></span>
    
1.  <span data-ttu-id="f7503-150">Dans l’Explorateur de solutions, pour afficher le code, ouvrez `MainWindow.xaml` file.</span><span class="sxs-lookup"><span data-stu-id="f7503-150">In the Solution Explorer, to display the code, open `MainWindow.xaml` file.</span></span>  <span data-ttu-id="f7503-151">Sélectionnez `F5` pour exécuter votre projet et afficher une fenêtre avec un bouton.</span><span class="sxs-lookup"><span data-stu-id="f7503-151">Select `F5` to run your project and show a window with a button.</span></span>  
    
## <span data-ttu-id="f7503-152">Étape 2: ajouter un contrôle WebView2 à votre projet</span><span class="sxs-lookup"><span data-stu-id="f7503-152">Step 2 - Add a WebView2 control to your project</span></span>  

<span data-ttu-id="f7503-153">Ensuite, ajoutez un contrôle WebView2 à votre projet.</span><span class="sxs-lookup"><span data-stu-id="f7503-153">Next add a WebView2 control to your project.</span></span>  

1.  <span data-ttu-id="f7503-154">Ouvrir `MainWindow.xaml` .</span><span class="sxs-lookup"><span data-stu-id="f7503-154">Open `MainWindow.xaml`.</span></span>  <span data-ttu-id="f7503-155">Ajoutez l’espace de noms XAML WebView2 en insérant la ligne suivante dans la `<Window/>` balise.</span><span class="sxs-lookup"><span data-stu-id="f7503-155">Add the WebView2 XAML namespace by inserting the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    <span data-ttu-id="f7503-156">Vérifiez que votre code `MainWindow.xaml` est semblable à l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="f7503-156">Confirm that your code in `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
    ```xml
    <Window
          x:Class="WinUI_Sample.MainWindow"
          xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
          xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
          xmlns:local="using:WinUI_Sample"
          xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
          xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
          mc:Ignorable="d"
          xmlns:controls="using:Microsoft.UI.Xaml.Controls"
          >
        
          <StackPanel Orientation="Horizontal" HorizontalAlignment="Center" VerticalAlignment="Center">
            <Button x:Name="myButton" Click="myButton_Click">Click Me</Button>
          </StackPanel>
    
    </Window>
    ```  
    
1.  <span data-ttu-id="f7503-157">Pour ajouter le contrôle WebView2, remplacez les `<StackPanel>` balises par l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="f7503-157">To add the WebView2 control, replace the `<StackPanel>` tags with the following code snippet.</span></span>  <span data-ttu-id="f7503-158">La `Source` propriété définit l’URI initial affiché dans le contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="f7503-158">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
    ```xml  
    <Grid>

        <Grid.RowDefinitions>
            <RowDefinition Height="Auto" />
            <RowDefinition Height="*" />
        </Grid.RowDefinitions>
        <Grid.ColumnDefinitions>
            <ColumnDefinition Width="*" />
            <ColumnDefinition Width="Auto" />
        </Grid.ColumnDefinitions>
        
        <controls:WebView2 x:Name="MyWebView"  Grid.Row="1" Grid.ColumnSpan="2" 
            Source="https://www.microsoft.com" HorizontalAlignment="Stretch" VerticalAlignment="Stretch" />
    
    </Grid>
    ```  
    
1.  <span data-ttu-id="f7503-159">Ouvrez `MainWindow.xaml.cs` et mettez en commentaire la ligne suivante.</span><span class="sxs-lookup"><span data-stu-id="f7503-159">Open `MainWindow.xaml.cs` and comment out the following line.</span></span>
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  <span data-ttu-id="f7503-160">Sélectionnez `F5` pour générer et exécuter votre projet.</span><span class="sxs-lookup"><span data-stu-id="f7503-160">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="f7503-161">Vérifiez que votre contrôle WebView2 s’affiche [https://www.microsoft.com][|::ref1::|Main] .</span><span class="sxs-lookup"><span data-stu-id="f7503-161">Confirm that your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="Contrôle WebView2 affichant le site microsoft.com" lightbox="./media/winui-gettingstarted-part3.png":::
       <span data-ttu-id="f7503-163">Un contrôle WebView2 affichant le site microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="f7503-163">A WebView2 control displaying the microsoft.com site.</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="f7503-164">Étape 3: ajouter des contrôles de navigation</span><span class="sxs-lookup"><span data-stu-id="f7503-164">Step 3 - Add navigation controls</span></span>  

<span data-ttu-id="f7503-165">Autorisez les utilisateurs à contrôler la page Web affichée dans votre contrôle WebView2 en ajoutant une barre d’adresse à votre application.</span><span class="sxs-lookup"><span data-stu-id="f7503-165">Allow users to control the web page that is displayed in your WebView2 control by adding an address bar to your app.</span></span>  

1.  <span data-ttu-id="f7503-166">Dans `MainWindow.xaml` , copiez et collez l’extrait de code suivant à l’intérieur de l' `Grid` élément qui contient l' `WebView2` élément.</span><span class="sxs-lookup"><span data-stu-id="f7503-166">In `MainWindow.xaml`, copy and paste the following code snippet inside the `Grid` element that contains the `WebView2` element.</span></span>  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    <span data-ttu-id="f7503-167">Vérifiez que votre `Grid` élément `MainWindow.xaml` est semblable à l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="f7503-167">Confirm that your `Grid` element of `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
    ```xml
    <Grid>
    
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto" />
            <RowDefinition Height="*" />
        </Grid.RowDefinitions>
        <Grid.ColumnDefinitions>
            <ColumnDefinition Width="*" />
            <ColumnDefinition Width="Auto" />
        </Grid.ColumnDefinitions>
    
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
        
        <WebView2 x:Name="MyWebView"  Grid.Row="1" Grid.ColumnSpan="2" 
            Source="https://www.microsoft.com" HorizontalAlignment="Stretch" VerticalAlignment="Stretch" />
    
    </Grid>
    ```  
    
1.  <span data-ttu-id="f7503-168">Dans l' `MainWindow.xaml.cs` extrait de code suivant, copiez l’extrait de code suivant `myButton_Click` , qui navigue dans le contrôle WebView2 à l’URL entrée dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="f7503-168">In `MainWindow.xaml.cs`, copy the following code snippet to `myButton_Click`, which navigates the WebView2 control to the URL entered in the address bar.</span></span>  
    
    ```csharp
    private void myButton_Click(object sender, RoutedEventArgs e)
    {
        try
        {
            Uri targetUri = new Uri(addressBar.Text);
            MyWebView.Source = targetUri;
        }
        catch (FormatException ex)
        {
            // Incorrect address entered.
        }
    }
    ```  
    
    <span data-ttu-id="f7503-169">Sélectionnez `F5` pour générer et exécuter votre projet.</span><span class="sxs-lookup"><span data-stu-id="f7503-169">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="f7503-170">Entrez une nouvelle URL dans la barre d’adresses, puis sélectionnez **atteindre**.</span><span class="sxs-lookup"><span data-stu-id="f7503-170">Enter a new URL in the address bar, and then choose **Go**.</span></span>  <span data-ttu-id="f7503-171">Par exemple, entrez `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="f7503-171">For example, enter `https://www.bing.com`.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f7503-172">Vérifiez que vous utilisez les URL complètes dans la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="f7503-172">Ensure you use complete URLs in the address bar.</span></span>  `ArgumentException` <span data-ttu-id="f7503-173">des exceptions sont levées si l’URL ne commence pas par `http://` ou `https://` .</span><span class="sxs-lookup"><span data-stu-id="f7503-173">exceptions are thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="Bing.com" lightbox="./media/winui-gettingstarted-bing.png":::
       <span data-ttu-id="f7503-175">Bing.com</span><span class="sxs-lookup"><span data-stu-id="f7503-175">Bing.com</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="f7503-176">Étape 4: événements de navigation</span><span class="sxs-lookup"><span data-stu-id="f7503-176">Step 4 - Navigation events</span></span>  

<span data-ttu-id="f7503-177">Les applications qui hébergent des contrôles WebView2 écoutent les événements suivants qui sont déclenchés par des contrôles WebView2 lors de la navigation dans la page Web.</span><span class="sxs-lookup"><span data-stu-id="f7503-177">Applications that host WebView2 controls listen for the following events that are raised by WebView2 controls during web page navigation.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> <span data-ttu-id="f7503-178">La redirection HTTP déclenche plusieurs `NavigationStarting` événements.</span><span class="sxs-lookup"><span data-stu-id="f7503-178">HTTP redirects raise multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="f7503-179">Pour plus d’informations, accédez à [événements de navigation][Webviews2ConceptsNavigationEvents].</span><span class="sxs-lookup"><span data-stu-id="f7503-179">For more information, navigate to [Navigation Events][Webviews2ConceptsNavigationEvents].</span></span>  

<span data-ttu-id="f7503-180">Lorsque des erreurs se produisent, les événements suivants sont déclenchés et peuvent accéder à une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="f7503-180">When errors occur, the following events are raised and may navigate to an error page.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
<span data-ttu-id="f7503-181">Pour obtenir un exemple d’utilisation des événements, inscrivez un gestionnaire pour `NavigationStarting` annuler toute demande qui n’utilise pas HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f7503-181">As an example of how to use the events, register a handler for `NavigationStarting` that cancels any request that does not use HTTPS.</span></span>  <span data-ttu-id="f7503-182">Dans `MainWindow.xaml.cs` l’exemple, modifiez le constructeur pour s’inscrire `EnsureHttps` , puis ajoutez la fonction pour qu' `EnsureHttps` il corresponde à l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="f7503-182">In `MainWindow.xaml.cs`, modify the constructor to register `EnsureHttps`, and add the `EnsureHttps` function so that it matches the following code snippet.</span></span>  

```csharp
public MainWindow()
{
    InitializeComponent();
    MyWebView.NavigationStarting += EnsureHttps;
}

private void EnsureHttps(WebView2 sender, WebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        args.Cancel = true;
    }
    else
    {
        addressBar.Text = uri;
    }
}
```  

<span data-ttu-id="f7503-183">Sélectionnez `F5` pour générer et exécuter votre projet.</span><span class="sxs-lookup"><span data-stu-id="f7503-183">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="f7503-184">Vérifiez que la navigation est bloquée sur les sites HTTP et qu’elle est autorisée pour les sites HTTPs.</span><span class="sxs-lookup"><span data-stu-id="f7503-184">Confirm that navigation is blocked to HTTP sites, and allowed for HTTPS sites.</span></span>  

## <span data-ttu-id="f7503-185">Étape 5: création de scripts</span><span class="sxs-lookup"><span data-stu-id="f7503-185">Step 5 - Scripting</span></span>  

<span data-ttu-id="f7503-186">Les applications hôtes risquent d’injecter du code JavaScript dans les contrôles WebView2 lors de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="f7503-186">Host applications may inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="f7503-187">Le JavaScript injecté s’applique à tous les nouveaux documents de niveau supérieur ainsi qu’aux trames enfant jusqu’à ce que le JavaScript soit supprimé.</span><span class="sxs-lookup"><span data-stu-id="f7503-187">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="f7503-188">Le JavaScript injecté s’exécute avec un minutage spécifique.</span><span class="sxs-lookup"><span data-stu-id="f7503-188">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="f7503-189">Exécutez-la après la création de l’objet global.</span><span class="sxs-lookup"><span data-stu-id="f7503-189">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="f7503-190">Exécutez-la avant d’exécuter tout autre script inclus dans le document HTML.</span><span class="sxs-lookup"><span data-stu-id="f7503-190">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="f7503-191">Par exemple, l’ajout de scripts envoie une alerte lorsqu’un utilisateur navigue vers des sites non HTTPs.</span><span class="sxs-lookup"><span data-stu-id="f7503-191">As an example, add scripts send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="f7503-192">Modifiez la `EnsureHttps` fonction pour injecter un script dans le contenu Web qui utilise [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].</span><span class="sxs-lookup"><span data-stu-id="f7503-192">Modify the `EnsureHttps` function to inject a script into the web content that uses [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].</span></span>  

```csharp
private void EnsureHttps(WebView2 sender, WebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        MyWebView.ExecuteScriptAsync($"alert('{uri} is not safe, try an https link')");
        args.Cancel = true;
    }
    else
    {
        addressBar.Text = uri;
    }
}
```  

<span data-ttu-id="f7503-193">Sélectionnez `F5` pour générer et exécuter votre projet.</span><span class="sxs-lookup"><span data-stu-id="f7503-193">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="f7503-194">Vérifiez que votre application affiche une alerte lorsque vous naviguez vers un site qui n’utilise pas HTTPs.</span><span class="sxs-lookup"><span data-stu-id="f7503-194">Confirm that your application displays an alert when you navigate to a site that does not use HTTPS.</span></span>  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="Contrôle WebView2 montrant une boîte de dialogue d’alerte" lightbox="./media/winui-gettingstarted-script.png":::
   <span data-ttu-id="f7503-196">Contrôle WebView2 montrant une boîte de dialogue d’alerte</span><span class="sxs-lookup"><span data-stu-id="f7503-196">WebView2 control showing an alert dialog</span></span>
:::image-end:::  

<span data-ttu-id="f7503-197">Félicitations, vous avez créé votre première application WebView2.</span><span class="sxs-lookup"><span data-stu-id="f7503-197">Congratulations, you built your first WebView2 app.</span></span>  

## <span data-ttu-id="f7503-198">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="f7503-198">Next Steps</span></span>  

<span data-ttu-id="f7503-199">Notre équipe génère actuellement plus d’API WebView2.</span><span class="sxs-lookup"><span data-stu-id="f7503-199">Our team is currently building more WebView2 APIs.</span></span>  <span data-ttu-id="f7503-200">Pour plus d’informations sur l’état actuel des API WebView2, accédez à la [spécification WebView2][GithubMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="f7503-200">For more information on the current state of WebView2 APIs, navigate to the [WebView2 spec][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  

> [!NOTE]
> <span data-ttu-id="f7503-201">L’objet WinRT CoreWebView2 peut ne pas être disponible au moment où les API WebView2 s’expédient.</span><span class="sxs-lookup"><span data-stu-id="f7503-201">The WinRT CoreWebView2 object may not be available at the time the WebView2 APIs ship.</span></span>  <span data-ttu-id="f7503-202">Pour comprendre les API disponibles pour les contrôles WebView2, accédez à [WebView2 spec][GithubMicrosoftUiXamlSpecsWebview2] pour obtenir la liste des API disponibles.</span><span class="sxs-lookup"><span data-stu-id="f7503-202">To understand which APIs are available to WebView2 controls, navigate to [WebView2 Spec][GithubMicrosoftUiXamlSpecsWebview2] for a list of the APIs that are available.</span></span>  

<span data-ttu-id="f7503-203">Pour plus d’informations sur les fonctionnalités d’WebView2, accédez à la [WebView2 de concepts et de How-To][Webview2IndexNextSteps] et aux [exemples de WebView2 référentiel Samples][GithubMicrosoftedgeWebview2samplesMain].</span><span class="sxs-lookup"><span data-stu-id="f7503-203">For more information about WebView2 capabilities, navigate to [WebView2 Concepts and How-To guides][Webview2IndexNextSteps] and the [WebView2 samples repo][GithubMicrosoftedgeWebview2samplesMain].</span></span>  

## <span data-ttu-id="f7503-204">Contacter l’équipe WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f7503-204">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2Index]: ../index.md "Introduction à Microsoft Edge WebView2 (Preview) | Documents Microsoft"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Étapes suivantes-présentation de Microsoft Edge WebView2 (Preview) | Documents Microsoft"  
[Webviews2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Événements de navigation | Documents Microsoft"  
[Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.Exeméthode cuteScriptAsync (chaîne) (Microsoft. Web. WebView2. WPF) | Documents Microsoft"  

[NugetConsumePackagesConfiguringNugetBehavior]: /nuget/consume-packages/configuring-nuget-behavior "Configurations NuGet communes Documents Microsoft"  

[UwpSchemasAppxpackageUapmanifestRoot]: /uwp/schemas/appxpackage/uapmanifestschema/schema-root "Référence du schéma de manifeste de package pour Windows 10 | Documents Microsoft"  

[VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]: /visualstudio/ide/finding-and-using-visual-studio-extensions#install-without-using-the-manage-extensions-dialog-box "Installer sans utiliser la boîte de dialogue gérer les extensions-gérer les extensions de Visual Studio | Documents Microsoft"  

[WindowsAppsWinui3ConfigureYourDevEnvironment]: /windows/apps/winui/winui3#configure-your-dev-environment "Configurer votre environnement de développement-bibliothèque d’interface utilisateur 3,0 Preview 1 (2020) | Documents Microsoft"  
[WindowsCommunitytoolkit]: /windows/communitytoolkit "Documentation sur le kit d’outils de la communauté Windows | Documents Microsoft"  
[WindowsMsixDesktopToUwpPackagingDotNet]: /windows/msix/desktop/desktop-to-uwp-packaging-dot-net "Configurer votre application de bureau pour MSIX Packaging dans Visual Studio | Documents Microsoft"  
[WindowsUwpGetStartedEnableYourDeviceForDevelopment]: /windows/uwp/get-started/enable-your-device-for-development "Activer votre appareil pour le développement | Documents Microsoft"  

[GithubMicrosoftUiXamlSpecsWebview2]: https://github.com/microsoft/microsoft-ui-xaml-specs/blob/master/active/WebView2/WebView2_spec.md "WebView2 spec-Microsoft/Microsoft-UI-XAML-spéc. GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Exemples de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftMain]: https://www.microsoft.com "Connaissances"  

[MicrosoftSupport12373]: https://support.microsoft.com/help/12373 "Windows Update: FAQ"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[NugetHome]: https://nuget.org "Accueil | Galerie NuGet"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X86]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe "Télécharger dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X64]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe " dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe"  

[VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]: https://marketplace.visualstudio.com/items?itemName=Microsoft-WinUI.WinUIProjectTemplates "Modèles de projet WinUI 3 | Visual Studio Marketplace"  
