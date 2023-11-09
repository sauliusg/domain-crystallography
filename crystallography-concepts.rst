Crystallography Concepts
========================

This file describes crystallography concepts based on the categories found in the DDLm Core CIF dictionary.

Main concepts
-------------

crystal (0)
...........

A crystal is a solid material which is adequately described by the following *scientific model*: the bulk of this solid body is composed of identical repeated units; these units fill the Euclidean space without gaps and without overlaps. The repeated unit us called a *unit cell* (crystallographic term) or a *fundamental domain* (mathematical term). See *cell*.

Unit cell (CIF category CELL (53 data names))
.............................................

The *unit cell*, defined in the CELL CIF category, describes a repeating unit of a crystal. This repeating unit fills 3D Euclidean space without the gaps and without the overlaps. The unit cells through the 3D space are related to each other by repeatedly translating along the three non-coplanar vectors \vec{a}, \vec{b} and \vec{c}; i.e. any translation \vec{T_{mnp}} = m\vec{a} + n\vec{b} + p\vec{c}, m,n,p \in \mathbb{Z} (𝐓ₘₙₚ=m𝐚+n𝐛+p𝐜, where m,n,p ∈ ℤ) maps any crystal cell into another identical crystal cell of the crystal. This mapping implies that the ideal crystal in this model is infinite, i.e. crystal boundary effects are not considered in the first approximation.

The \vec{T_{mnp}} (𝐓ₘₙₚ) translation vectors map the crystal (Euclidean space) in to itself and form a translation symmetry group of the crystal. 

In the physical model of the crystal, the unit cell is considered to be filled by physical entities such like elementary particles (electrons, nuclei). For the purpose of describing the X-ray scattering experiments, the unit cell can be considered to be filled by continuous electron density. For neutron scattering experiments, the cell is filled with nucleon density, described as scattering length density.

Atom and Atom site (CIF category ATOM_SITE (53 data names))
...........................................................

In most cases, the *unit cell* can be assumed to be filled by spherically symmetric atoms (*spherical atom model*), consisting of a spherically symmetric electron cloud (for X-ray scattering), or a delta-function like nucleus (for neutron scattering). The electron density or the scattering length density in the unit cell (and, consequently by repetition using 𝐓ₘₙₚ translations) is then obtained by simple arithmetic sum of densities from individual atoms. Each atom is described by its position in the unit cell, given by 3D coordinates of the sphere centre, an atom type that implies certain density distribution for this atom (identical for all atoms of the given type), and additional parameters (occupancy, TDP) needed to describe scattering experiments precisely. Together these coordinates and additional parameters describe an *atom site* in a unit cell.

It is tacitly assumed that the atoms in the unit cell of the crystal (described in CIFs) are the same atoms that chemists consider when modelling structure and chemical properties of compounds.

Reflection (CIF categories REFLN (44 data names), DIFFRN_REFLN (41 data names))
...............................................................................

A beam of the incident radiation is reflected from the *crystal* in discrete directions (so called Bragg *reflections*). Each direction under which the beam is reflected (scattered) is identified by three integer numbers (*indices*).  h, k and l (h,k,l ∈ ℤ). The h,k,l indices constitute coordinates of a *reciprocal lattice* node in *reciprocal space*.

Each reflection is characterised by two numbers: the amplitude and the phase, which correspond to (strictly speaking, are (structure) *factor* of) the amplitude and the phase of the scattered monochromatic radiation beam. Current experimental equipment, however, records only the *intensity* of the scattered beams, thus the amplitude and the phase are derived quantities.

Atom type (CIF category ATOM_TYPE_SCAT (39 data names))
.......................................................

The atom type found at given *atom sites* of the unit cell. For the purposes of crystallography, i.e. for describing outcomes of a scattering experiment, the only relevant information is atomic scattering factors. It is tacitly assumed however that the atoms at sites are precisely the chemist's atoms that are used in chemical modelling and that are described in the Periodic Table of Elements.

There are cases when in a crystal two different atoms can be found at the same atom site in different unit cells. Strictly speaking, such material is no longer periodic, but it can be modelled as periodic if a special "atom type" which is mixture of several *chemical atoms types*, and possibly a vacancy, is considered. Such crystal is said to have *substitutional disorder*. The chemical atom types however are still assumed to be the same those used for chemical models and taken from the Periodic Table of Elements.

chemical (33)
.............

exptl_crystal (31)
diffrn (29)

diffrn_reflns (23)
reflns (21)
space_group (19)
model_site (19)

geom_hbond (16)
atom_type (16)

exptl (12)
geom (10)

valence_param (9)

chemical_formula (8)

space_group_symop (7)

atom (7)
refine_diff (6)

atom_sites (6)
space_group_wyckoff (5)

display_colour (5)

model (3)

exptl_crystal_appearance (3)

diffraction (3)

valence (2)
structure (2)

Auxiliary concepts
------------------

refine_ls (47)
atom_site_aniso (45)

atom_sites_fract_transform (29)
atom_sites_cartn_transform (29)

reflns_shell (16)

diffrn_orient_refln (16)

geom_torsion (14)

exptl_crystal_face (14)
geom_angle (12)

diffrn_source (12)
cell_measurement (12)

reflns_class (11)
geom_bond (11)
diffrn_orient_matrix (11)

diffrn_reflns_transf_matrix (10)
diffrn_radiation (10)

refine_ls_class (8)
geom_contact (8)
diffrn_standards (8)
diffrn_radiation_wavelength (8)

atom_analytical (8)
reflns_scale (7)
function (7)
exptl_absorpt (7)
diffrn_reflns_class (7)
diffrn_measurement (7)

chemical_conn_atom (7)
atom_analytical_mass_loss (7)

cif_core (6)

cell_measurement_refln (6)

diffrn_standard_refln (5)
diffrn_detector (5)

chemical_conn_bond (5)

atom_scat_versus_stol (4)
atom_analytical_source (4)
refine (3)

diffrn_scale_group (3)
diffrn_attenuator (3)

space_group_generator (2)
diffrn_orient (2)

display (1)
core_dic (1)

Metadata concepts
-----------------

citation (27)

journal (22)
publ_section (17)

audit (12)

database_code (11)
publication (10)
journal_date (10)

publ_author (9)
publ_contact_author (8)

publ (7)

computing (7)
audit_author (7)

audit_support (6)
audit_contact_author (6)

publ_body (5)

database_related (5)
database (5)

publ_manuscript (4)
journal_index (4)

publ_requested (3)
publ_manuscript_incl_extra (3)

citation_editor (3)
citation_author (3)
audit_conform (3)
audit_author_role (3)

valence_ref (2)

audit_link (2)

Auxiliary metadata concepts
---------------------------

journal_techeditor (7)
journal_coeditor (7)


Unclassified concepts
---------------------


# Local Variables:
# visual-line-mode: t
# auto-fill-mode: 0
# fill-column: 70000
# End:
