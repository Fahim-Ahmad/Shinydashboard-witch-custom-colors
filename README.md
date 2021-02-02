## Dashboard with custom colors

```r
library(shiny)
library(shinydashboard)

ui <- dashboardPage(
  dashboardHeader(),
  dashboardSidebar(),
  dashboardBody(
    HTML("<h2 style='color:darkred; text-align:center'>Shinydashboard with custom <i>sidebar</i> and <i>navbar</i> color</h2>")
  ),
  tags$head(
    tags$style(HTML("
           .skin-blue .main-header .logo {background-color: black;}
           .skin-blue .main-header .logo:hover {background-color: black;}
           .skin-blue .main-header .navbar {background-color: darkred;}
           .skin-blue .main-header .navbar .sidebar-toggle:hover{background-color: darkred;}
           .skin-blue .main-sidebar { background-color:  green;}
           "))
  )
)

server <- function(input, output){}

shinyApp(ui, server)
```
