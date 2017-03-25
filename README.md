# WpfExtendedToolkit DataGrid Czech Language



Počeštění DataGridu WPF Extended Toolkitu (http://wpftoolkit.codeplex.com/)
 v3.0

## Použití:

Je třeba mít referencovaný wpftoolkit (ať už stažený nebo NuGet). Vytvořeno pro verzi 3.0

ResourceDictionary z tohoto repozitáře je třeba přidat jako MergedDictionary do Resource, například takto:

    <UserControl x:Class="(...)"
                 xmlns:xcdgm="clr-namespace:Xceed.Wpf.DataGrid.Markup;assembly=Xceed.Wpf.DataGrid" />
      <UserControl.Resources>
        <ResourceDictionary>
          <ResourceDictionary.MergedDictionaries>

            <xcdgm:DataGridThemeResourceDictionary Source="/myAssembly;component/Themes/xcdg.cz.xaml" />

          </ResourceDictionary.MergedDictionaries>
        </ResourceDictionary>
      </UserControl.Resources>
    </UserControl>

A to je vše.


Nyní můžete zvesela používat DataGridControl, například takto:

    <UserControl x:Class="(...)"
                 xmlns:xcdgm="clr-namespace:Xceed.Wpf.DataGrid.Markup;assembly=Xceed.Wpf.DataGrid" />
      <UserControl.Resources>
        <ResourceDictionary>
          <ResourceDictionary.MergedDictionaries>

            <xcdgm:DataGridThemeResourceDictionary Source="/myAssembly;component/Themes/xcdg.cz.xaml" />

          </ResourceDictionary.MergedDictionaries>
        </ResourceDictionary>
      </UserControl.Resources>


      <xcdg:DataGridControl ItemsSource="{Binding Path=FilteredView}">
        <xcdg:DataGridControl.Columns>
          <xcdg:Column FieldName="DateString"
                       ReadOnly="True"
                       IsMainColumn="True"
                       Title="Datum" />
          <xcdg:Column FieldName="Length"
                       ReadOnly="True"
                       Title="Délka" />
          <xcdg:Column FieldName="Project"
                       ReadOnly="True"
                       Title="Projekt" />
        </xcdg:DataGridControl.Columns>
      </xcdg:DataGridControl>
    </UserControl>
