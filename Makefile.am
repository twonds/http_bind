AUTOMAKE_OPTIONS = subdir-objects

EJABBERD_PREFIX=$(libdir)/ejabberd

ESRCDIR=$(top_srcdir)/src/web
EBINDIR=$(top_builddir)/ebin

mod_http_bind_FILES = mod_http_bind.erl ejabberd_http_bind.erl
mod_http_bind_BEAMS = mod_http_bind.beam ejabberd_http_bind.beam

EXTRA_DIST = ${addprefix $(ESRCDIR)/, $(mod_http_bind_FILES)}

mod_http_binddir = $(EJABBERD_PREFIX)/ebin
mod_http_bind_DATA = ${addprefix $(EBINDIR)/, $(mod_http_bind_BEAMS)}
CLEANFILES = $(mod_http_bind_DATA)


$(EBINDIR)/%.beam:
	$(ERLC) $(ERLCFLAGS) -b beam -o $(EBINDIR) $(ESRCDIR)/*.erl


