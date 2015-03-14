tls-milter is developed on assignment from Skatteverket (the Swedish National Taxboard) to
add the possibility to check if enforced TLS is activated and available to a specific site/domain for a "flagged" recipient.

If enforced TLS is configured and available, the milter leaves the delivery up to the MTA, if it isn't available, the milter will force a return of a NDR (non-delivery report) to the sender with an URL to assist the sender.

By default, tls-milter looks for a prepended "s:" to any recipient, e.g.: mail to s:user@domain.cc will only be delivered if the MTA responsible for the delivery have enforced TLS configured for the domain "domain.cc".

The project is fully coded in Perl and the code has been developed and released as GPLv3, to ensure that other agencies or the public could possibly benefit from it.