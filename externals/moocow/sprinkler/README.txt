    README for pd external 'sprinkler' (formerly 'forward')

DESCRIPTION
    'sprinkler' objects do dynamic control-message dissemination.

    Given a list as input, a 'sprinkler' object interprets the initial list
    element as the name of a 'receive' object, and [send]s the rest of the
    list to that object.

INSTALLATION
    Issue the following commands to the shell:

       cd sprinkler-X.YY  (or wherever you extracted the distribution)
       ./configure
       make
       make install

BUILD OPTIONS
    The 'configure' script supports the following options, among others:

    --enable-debug , --disable-debug
        Whether to enable verbose debugging messages. Default=no.

    --enable-forward , --disable-forward
        Whether to create [forward] objects as instances of the [sprinkler]
        class (MAX-incompatible). Default=no.

    --enable-all-forwardmess , --disable-all-forwardmess
        Whether to use pd_forwardmess() for all messages. If this option is
        disabled (the default), messages of length 1 will be handled
        specially; thus a symbol 'foo' will be passed as 'symbol foo',
        rather than just 'foo'.

        Default=no.

        Future versions of 'sprinkler' may use pd_forwardmess() for all
        messages by default -- go on, try it!

ACKNOWLEDGEMENTS
    PD by Miller Puckette and others.

    Ideas, black magic, and other nuggets of information drawn from code by
    Guenter Geiger, Larry Troxler, and iohannes m zmoeling.

    Thanks to Krzysztof Czaja for pointing out to me the existence of MAX
    "forward", and to Miller Puckette for the name "sprinkler".

    Thanks to Erasmus Zipfel for a bugreport and useful ideas.

KNOWN BUGS
    One of the acknowledgements used to be in this section. Sorry, folks.

    Backwards-compatible version is incompatible with MAX.

    Semantic strangeness with singleton messages is somewhat cryptic.

AUTHOR
    Bryan Jurish <moocow@ling.uni-potsdam.de>

