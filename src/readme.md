sass/ 
| 
|– base/ 
|    | 
|    |– _reset.scss         # Reset/normalize 
|    |– _typography.scss    # Typography rules 
|    ...                   # Etc… 
| 
|– components/ 
|    |– _buttons.scss       # Buttons 
|    |– _carousel.scss      # Carousel 
|    |– _cover.scss         # Cover 
|    |– _dropdown.scss      # Dropdown 
|    |– _navigation.scss    # Navigation 
|    ...                   # Etc… 
| 
|– helpers/ 
|    |– _variables.scss     # Sass Variables 
|    |– _functions.scss     # Sass Functions 
|    |– _mixins.scss        # Sass Mixins 
|    |– _helpers.scss       # Class & placeholders helpers 
|    ...                   # Etc… 
|   
|– layout/ 
|     |– _grid.scss         # Grid system 
|     |– _header.scss       # Header 
|     |– _footer.scss       # Footer 
|     |– _sidebar.scss      # Sidebar 
|     |– _forms.scss        # Forms 
|     ...                  # Etc… 
| 
|– pages/ 
|     |– _home.scss         # Home specific styles 
|     |– _contact.scss      # Contact specific styles 
|      ...                 # Etc… 
| 
|– themes/ 
|     |– _theme.scss        # Default theme 
|     |– _admin.scss        # Admin theme 
|     ...                  # Etc… 
| 
|– vendors/ 
|     |– _bootstrap.scss    # Bootstrap 
|     |– _jquery-ui.scss    # jQuery UI 
|     ...                  # Etc… 
|     
| 
`– main.scss 

Base
base/文件夹包含了一些有关于你的项目中一些模板相关。在这里，你可以看到reset样式(或者Normalize.css,或者其他)，也有一些关于文本排版方面的，当然根据不同的项目会有一些其他的文件。

Helpers
helpers/文件夹（有的地方也称其为utils/）主要包含了项目中关于Sass的工具和帮助之类。在里面放置了我们需要使用的_function.scss，和_mixin.scss。在这里还包含了一个_variables.scss文件（有的地方也称其为_config.scss），这里包含项目中所有的全局变量（比如排版本上的，配色方案等等）。

_variables.scss
_mixin.scss
_function.scss
_placeholders.scss(也有称为_helpers.scss)
Layout
layout/文件夹(有时也称为partials/)中放置了大量的文件，每个文件主要用于布局方面的，比如说"header"，“footer”等。他也会包括_grid.scss文件，用来创建网格系统。

_grid.scss
_header.scss
_footer.scss
_sidebar.scss
_forms.scss
导航文件（_navigation.scss）文件放在这里也有意义，虽然我将他放在了components/文件夹中。但是我想将其放在layout/文件夹中更好些，当然最后还是由你自己来决定。

Components
对于一些小组件，都放在了components/文件夹（通常也称为modules/），layout/是一个宏观的（定义全局的线框），components/是一个微观的。它里面放了一些特定的组件，比如说slider，loading，widget或者其他的小组件。通常components/目录下的都是一些小组件文件。

_media.scss
_carousel.scss
_thumbnails.scss
Page
如果你需要针对一些页面写特定的样式，我想将他们放在page/文件夹中是非常酷的，并且以页面的名称来命名。例如，你的首页需要制作一个特定的样式，那么你就可以在page/文件夹中创建一个名叫_home.scss文件。

_home.scss
_contact.scss
根据你自己的布署，你可以根据自己的需求调用这些文件，避免与其他样式文件合并在一起。这真的主取决于你自己，在我工作的地方，我是不允许这样的事情发生，只在需要的页面调用需要的文件。比如说，我们首页有一个特定的布局样式，编译出来的CSS大约有200行代码。为了防止每个页面加载这些代码，我只在主页文件上引用这个文件。

Themes
如果你像我一样要为一个大型的网站制作多个主题，那么有一个theme/文件夹是非常有意义的。你可以把主题相关的文件放在这个文件夹中。这绝对跟具体的项目有关，你只要觉得跟主题相关的，有必要引入。

_theme.scss
_admin.scss
Vendors
最后一个但并非不重要，创建vendors/文件夹，主要用来包含来自外部的库和框架的CSS文件。比如Bootstrap,jQueryUI，FancyCarouselSliderjQueryPowered等等。把这些文件放在同一个文件夹中，你可以说，嘿，这些代码不是我的，不是我写的，跟我无关。

例如：
bootstrap.scss
jquery-ui.scss
select2.scss