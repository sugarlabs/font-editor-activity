[![Build Status](https://travis-ci.org/sugarlabs/edit-fonts-activity.svg?branch=master)](https://travis-ci.org/sugarlabs/edit-fonts-activity)

# Sugar Activity: Edit Fonts Activity

Project Blog: <http://sugarlabs.github.io/edit-fonts-activity/>

Typeface design is a cornerstone of literate cultures, with subliminal power: 
Typefaces carry the emotions of texts, from formal designs that speak with authority to fun designs that are silly or military or ornate.
They are both artistic and functional works, and our ability to share and modify them is important for the same reasons as for software programs.

Sugar is a learning platform that reinvents how computers are used for education. 
Collaboration, reflection, and discovery are integrated directly into the user interface, and “studio thinking” and “reflective practice” are promoted through Sugar’s clarity of design. 
Sugar was initially developed by Red Hat and Pentagram with One Laptop per Child, and today is developed by the Sugar Labs community. 
It now has over 1M users, including every child in Uruguay.

Fonts are fun to make, and Sugar needs a font editor activity so learners can make and modify them for their own tastes and needs.

## Project News

* [Week 1 Work](https://sugarlabs.github.io/edit-fonts-activity/week-1-work)
* [Week 2+3 Work](https://sugarlabs.github.io/edit-fonts-activity/week-3-work)
* [Week 4 Work](https://sugarlabs.github.io/edit-fonts-activity/week-4-work)
* [Week 5 Work](https://sugarlabs.github.io/edit-fonts-activity/week-5-work)
* [Week 6 Work](https://sugarlabs.github.io/edit-fonts-activity/week-6-work)

The feature list of the application is documented on the project blog. 

## Usage

Download this repo to a Sugar desktop and set it up, then launch it from the Home screen. 

    # boot Fedora-Live-SoaS-x86_64-23-10.iso
    sudo dnf install git -y;
    git clone http://https://github.com/sugarlabs/edit-fonts-activity.git;
    cd edit-fonts-activity;
    python setup.py dev
    # go to home, list view, search Fonts

## Development

To develop the Activity, your changes must conform to the [PEP8 style guide](https://www.python.org/dev/peps/pep-0008/). 
We use Travis CI to enforce this; the following command is run on every pull request and it must run without outputting any errors:

    flake8 --ignore=E402 --statistics \
     --exclude=defcon,extractor,fontTools,fontmake,robofab,\
     ufo2ft,ufoLib,snippets,localIcon .

The `--statistics` argument prints a list at the end showing the total count of each error category at the end. 

To eliminate all errors, it is helpful to see the total number of errors for each file:

    flake8 --ignore=E402 \
    --exclude=defcon,extractor,fontTools,fontmake,robofab,\
    ufo2ft,ufoLib,snippets,localIcon  . \
    | cut -d: -f1 | sort | uniq -c | sort;

To eliminate a specific error, it is helpful to filter the output using grep:

    flake8 --ignore=E402 \
    --exclude=defcon,extractor,fontTools,fontmake,robofab,\
    ufo2ft,ufoLib,snippets,localIcon  . \
    | grep W291; # trailing whitespace

## License

GPLv3
