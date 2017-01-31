rc - Windows resource compiler library
================================================

rc is a development component that allows to compile text representaion of resource data into binary representation. The binary represenation is then linked to target executable file via link utility.

Currently the rc project is separated to following sub-projects:
- /rc/src/ (static library) - contains generic logics of resource compiler including parser, default directives and so on.
- /rc/platforms/windows/dll (dynamic library) - dll wrapper that exports resource compiler API through dll exports.
- /rc/platforms/windows/exe (executable) - an executable file that performs command line parsing, setting up library context and performing all required operations e.g. compiling or checking input files. Depending on compile-time options, it uses either static or dynamic library version of rc component.
- /rc/drivers/ (drivers) - this folder contains extensions to the rc library, for example, custom directives or connection to different preprocessor utility (by default, the internal preprocessor is used).

