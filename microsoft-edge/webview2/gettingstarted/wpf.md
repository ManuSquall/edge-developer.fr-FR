---
description: Guide de mise en route de WebView2 pour les applications WPF
title: Mise en route de WebView2 pour les applications WPF
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, applications WPF, WPF, Edge, CoreWebView2, contrôle de navigateur, html Edge, mise en route, mise en route, .NET
ms.openlocfilehash: e928dae0aa63f15ca5fa21860c83fa5529e905df
ms.sourcegitcommit: fab44f7e183a3c4f12bf925512fc62d84a4d6edc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182373"
---
# Commencer à utiliser WebView2 dans WPF

Dans cet article, vous allez commencer à créer votre première application WebView2 et à découvrir les principales fonctionnalités de [WebView2](../index.md).  Pour plus d’informations sur les API individuelles, voir informations de référence sur les [API](/dotnet/api/microsoft.web.webview2.wpf).  

## Conditions préalables  

Vérifiez que vous avez installé la liste des conditions préalables suivantes avant de continuer:  

* [WebView2 Runtime][Webview2Installer] ou un canal de l’alphabet [Microsoft Edge (chrome) non stable](https://www.microsoftedgeinsider.com/download) installé sur windows 10, Windows 8,1 ou Windows 7.  
* [Visual Studio](https://visualstudio.microsoft.com) 2017 ou version ultérieure.  

## Étape 1: créer une application de fenêtre unique  

Utiliser un projet de bureau de base contenant une seule fenêtre principale.  

1.  Ouvrez **Visual Studio**.  
1.  Sélectionnez application **WPF .net Core** ou **application WPF .NET Framework**, puis sélectionnez **suivant**.  
    
    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpfcore.png" alt-text="Noyau WPF":::
             Noyau WPF :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpffw.png" alt-text="Infrastructure WPF":::
             Infrastructure WPF :::image-end:::
       :::column-end:::
    :::row-end:::
    
1.  Entrez des valeurs pour le nom et l' **emplacement**du **projet** .  Sélectionnez .NET Framework 4.6.2 ou version ultérieure, ou .NET Core 3,0 ou version ultérieure.  
    
    :::row:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createcore.png" alt-text="Créer un cœur":::
                 Créer un cœur :::image-end:::
           :::column-end:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createfw.png" alt-text="Créer une infrastructure":::
                 Créer une infrastructure :::image-end:::
           :::column-end:::
        :::row-end:::
    
1.  Sélectionnez **créer** pour créer votre projet.  
    
## Étape 2: installer le SDK WebView2  

Ensuite, ajoutez le kit de développement logiciel (SDK) WebView2 au projet en utilisant NuGet.  

1.  Ouvrez le menu contextuel du projet \ (cliquez avec le bouton droit sur \), puis sélectionnez **gérer les packages NuGet...**.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="NuGet":::
       NuGet
    :::image-end:::
    
1.  Entrez `Microsoft.Web.WebView2` dans la barre de recherche.  Sélectionnez **Microsoft. Web. WebView2** dans les résultats de la recherche.  
   
     ![NuGet](./media/installnuget.PNG)
    
    Pour commencer à développer des applications à l’aide de l’API WebView2, vous avez terminé.  Sélectionnez `F5` pour générer et exécuter le projet.  Le projet en cours d’exécution affiche une fenêtre vide.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-blank.png" alt-text="Application vide":::
       Application vide
    :::image-end:::  
    
## Étape 3: créer un WebView unique dans MainWindow. Xaml  

Ensuite, ajoutez un WebView à votre application.  

1.  Ouvrir `MainWindow.xaml` .  Ajoutez l’espace de noms XAML WebView2 en insérant la ligne suivante dans la `<Window/>` balise.  
    
    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  
    
    Vérifiez que le code `MainWindow.xaml` ressemble à l’extrait de code suivant.  
    
    ```xml
    <Window x:Class="WPF_Getting_Started.MainWindow"
            xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
            xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
            xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
            xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
            xmlns:local="clr-namespace:{YOUR PROJECT NAME}"
            xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
            mc:Ignorable="d"
            Title="MainWindow"
            Height="450"
            Width="800"
    >
        <Grid>
        
        </Grid>
    </Window>
    ```  
    
1.  Ajoutez le contrôle WebView2 en remplaçant les `<Grid>` balises par l’extrait de code suivant.  La `Source` propriété définit l’URI initial affiché dans le contrôle WebView2.  
    
    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  
    
1.  Appuyez `F5` pour générer et exécuter votre projet.  Vérifiez que votre contrôle WebView2 s’affiche [https://www.microsoft.com](https://www.microsoft.com) .  
    
    :::image type="complex" source="./media/wpf-gettingstarted-microsoft.png" alt-text="Microsoft.com":::
       Microsoft.com
    :::image-end:::  
    
## Étape 4: navigation  

Ajoutez la possibilité d’autoriser les utilisateurs à modifier l’URL d’affichage du contrôle WebView2 en ajoutant une barre d’adresse à l’application.

1.  Dans **MainWindow. Xaml**, ajoutez une barre d’adresse en copiant et en collant l’extrait de code suivant à l’intérieur du DockPanel qui contient le WebView.  
    
    ```xml
    <DockPanel DockPanel.Dock="Top">
        <Button x:Name="ButtonGo"
                DockPanel.Dock="Right"
                Click="ButtonGo_Click"
                Content="Go"
        />
        <TextBox Name="addressBar"/>
    </DockPanel>
    ```  
    
    Vérifiez que la `DockPanel` section de l' `MainWindow.xaml` extrait de code suivant ressemble à ceci.  
    
    ```xml
    <DockPanel>
        <DockPanel DockPanel.Dock="Top">
            <Button x:Name="ButtonGo" DockPanel.Dock="Right" Click="ButtonGo_Click" Content="Go"/>
            <TextBox Name = "addressBar"/>
        </DockPanel>
        <wv2:WebView2 Name = "webView"
                      Source = "https://www.microsoft.com"
        />
    </DockPanel>
    ```  
    
1.  Ouvrir `MainWindow.xaml.cs` dans Visual Studio.  Ajoutez l' `CoreWebView2` espace de noms en insérant l’extrait de code suivant en haut de `MainWindow.xaml.cs` .  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```
    
1.  Dans **MainWindow.Xaml.cs**, copiez l’extrait de code suivant afin de créer la `ButtonGo_Click` méthode, qui permet d’accéder à l’URL entrée dans la barre d’adresses.  
    
    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  
    
    Appuyez `F5` pour générer et exécuter votre projet.  Entrez une nouvelle URL dans la barre d’adresses, puis sélectionnez **atteindre**.  Par exemple, entrez `https://www.bing.com` .  Vérifiez que le contrôle WebView2 accède à l’URL.  
    
    > [!NOTE]
    > Vérifiez qu’une URL complète est entrée dans la barre d’adresses.  `ArgumentException`A est levé si l’URL ne commence pas par `http://` ou `https://` .  
    
    :::image type="complex" source="./media/wpf-gettingstarted-bing.png" alt-text="Bing":::
       Bing
    :::image-end:::
    
## Étape 5: événements de navigation  

Lors de la navigation de la page Web, le contrôle WebView2 déclenche des événements. L’application qui héberge les contrôles WebView2 écoute les événements suivants.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

Pour plus d’informations, voir [événements de navigation](../concepts/navigation-events.md).  

:::image type="complex" source="../media/navigation-events.png" alt-text="Événements de navigation":::
   Événements de navigation
:::image-end:::  

Lorsqu’une erreur se produit, les événements suivants sont déclenchés et peut dépendre de la navigation sur une page d’erreur.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

Lorsqu’il existe une redirection HTTP, il existe plusieurs `NavigationStarting` événements.  

Pour illustrer l’utilisation de ces événements, commencez par enregistrer un gestionnaire pour `NavigationStarting` Annuler toutes les demandes qui n’utilisent pas HTTPS.  

Dans `MainWindow.xaml.cs` , modifiez le constructeur comme illustré ci-dessous, puis ajoutez la `EnsureHttps` fonction.  

```csharp
public MainWindow()
{
    InitializeComponent();
    webView.NavigationStarting += EnsureHttps;
}

void EnsureHttps(object sender, CoreWebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        args.Cancel = true;
    }
}
```  

Dans le constructeur, EnsureHttps est enregistré en tant que gestionnaire d’événements sur l' `NavigationStarting` événement sur le contrôle WebView2.  

Appuyez `F5` pour générer et exécuter votre projet.  Confirmez que lorsque vous naviguez vers un site HTTP, le WebView **reste inchangé**.  Toutefois, le WebView navigue vers les sites HTTPs.  

## Étape 6: création de scripts  

Vous pouvez utiliser des applications hôtes pour injecter du code JavaScript dans les contrôles WebView2 lors de l’exécution.  Le JavaScript injecté s’applique à tous les nouveaux documents de niveau supérieur ainsi qu’à toute image enfant, jusqu’à ce que le JavaScript soit supprimé.  Le JavaScript injecté est exécuté après la création de l’objet global et avant les scripts inclus dans le document HTML.  

Vous pouvez utiliser les scripts pour alerter l’utilisateur lorsque vous naviguez vers un site non HTTPs.  Modifiez la `EnsureHttps` fonction de telle sorte qu’elle injecte le script dans le contenu Web à l’aide de la méthode [ExecuteScriptAsync](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync) .  

```csharp
void EnsureHttps(object sender, CoreWebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        webView.CoreWebView2.ExecuteScriptAsync($"alert('{uri} is not safe, try an https link')");
        args.Cancel = true;
    }
}
```  

Appuyez `F5` pour générer et exécuter votre projet.  Vérifiez que l’application affiche une alerte lorsque vous naviguez vers un site qui n’utilise pas HTTPs.  

:::image type="complex" source="./media/wpf-gettingstarted-https.png" alt-text="HTTPS":::
   HTTPS
:::image-end:::  

## Étape 7: communication entre l’hôte et le contenu Web  

L’hôte et le contenu Web sont en mesure de communiquer entre eux `postMessage` comme suit:  

*   Le contenu Web d’un contrôle WebView2 risque de publier un message destiné à l’hôte à l’aide de `window.chrome.webview.postMessage` .  L’hôte gère le message en utilisant tout inscrit `WebMessageReceived` sur l’hôte.  
*   Héberge les messages dans le contenu Web d’un contrôle WebView2 en utilisant `CoreWebView2.PostWebMessageAsString` ou `CoreWebView2.PostWebMessageAsJSON` .  Ces messages sont interceptés par des gestionnaires ajoutés à `window.chrome.webview.addEventListener` .  

Ce mécanisme de communication permet au contenu Web de transmettre des messages à l’hôte à l’aide de fonctionnalités natives.  

Dans votre projet, lorsque le contrôle WebView2 navigue vers une URL, il affiche l’URL dans la barre d’adresse et avertit l’utilisateur de l’URL qui s’affiche dans le contrôle WebView2.  

1.  Dans **MainWindow.Xaml.cs**, mettez à jour votre constructeur et créez une `InitializeAsync` fonction comme illustré dans l’extrait de code suivant.  La `InitializeAsync` fonction est en attente [EnsureCoreWebView2Async](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) , car l’initialisation de `CoreWebView2` est asynchrone.  
    
    ```csharp
    public MainWindow()
    {
        InitializeComponent();
        webView.NavigationStarting += EnsureHttps;
        InitializeAsync();
    }
    
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
    }
    ```  
    
1.  Une fois **CoreWebView2** initialisé, inscrivez un gestionnaire d’événements pour y répondre `WebMessageReceived` .  Dans **MainWindow.Xaml.cs**, mettez à jour `InitializeAsync` et ajoutez à `UpdateAddressBar` l’aide de l’extrait de code suivant.  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
    }
    
    void UpdateAddressBar(object sender, CoreWebView2WebMessageReceivedEventArgs args)
    {
        String uri = args.TryGetWebMessageAsString();
        addressBar.Text = uri;
        webView.CoreWebView2.PostWebMessageAsString(uri);
    }
    ```  
    
1.  Pour que le WebView envoie un message électronique et y réponde, une fois l' `CoreWebView2` initialisation terminée, l’hôte:  
    
    1.  Injecte un script dans le contenu Web qui inscrit un gestionnaire pour imprimer le message à partir de l’hôte.  
    1.  Injecte un script dans le contenu Web qui publie l’URL vers l’hôte.  
    
    Dans la `MainWindow.xaml.cs` mise à jour, `InitializeAsync` procédez comme suit:  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
        
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
    }
    ```  
    
    Appuyez `F5` pour générer et exécuter l’application.  À présent, la barre d’adresses affiche l’URI dans le contrôle WebView2. Lorsque vous parvenez à un nouvel URI, le contrôle WebView2 avertit l’utilisateur de l’URI affiché dans le contrôle WebView2.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-searchbar.png" alt-text="addressBar":::
       addressBar
    :::image-end:::

Félicitations, vous avez créé votre première application WebView2.  

## Étapes suivantes  

*   Pour obtenir un exemple complet de fonctionnalités WebView2, voir [WebView2Samples référentiel Samples](https://github.com/MicrosoftEdge/WebView2Samples) sur GitHub.  
*   Pour plus d’informations sur les API WebView2, voir informations de référence sur les [API](/dotnet/api/microsoft.web.webview2.wpf.webview2).  
*   Pour plus d’informations sur WebView2, voir [ressources WebView2](../index.md#next-steps).  

## Contacter l’équipe WebView de Microsoft Edge  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  


<!-- links -->  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Programme d’installation de WebView2" 
