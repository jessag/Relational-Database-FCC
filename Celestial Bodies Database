--
-- PostgreSQL database dump
--

-- Dumped from database version 12.9 (Ubuntu 12.9-2.pgdg20.04+1)
-- Dumped by pg_dump version 12.9 (Ubuntu 12.9-2.pgdg20.04+1)

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

DROP DATABASE universe;
--
-- Name: universe; Type: DATABASE; Schema: -; Owner: freecodecamp
--

CREATE DATABASE universe WITH TEMPLATE = template0 ENCODING = 'UTF8' LC_COLLATE = 'C.UTF-8' LC_CTYPE = 'C.UTF-8';


ALTER DATABASE universe OWNER TO freecodecamp;

\connect universe

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

SET default_tablespace = '';

SET default_table_access_method = heap;

--
-- Name: black_hole; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.black_hole (
    name character varying(30),
    discovery_year integer,
    galaxy_id integer,
    black_hole_id integer NOT NULL,
    description text DEFAULT 'lorem ipsum...'::text NOT NULL
);


ALTER TABLE public.black_hole OWNER TO freecodecamp;

--
-- Name: black_hole_black_hole_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.black_hole_black_hole_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.black_hole_black_hole_id_seq OWNER TO freecodecamp;

--
-- Name: black_hole_black_hole_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.black_hole_black_hole_id_seq OWNED BY public.black_hole.black_hole_id;


--
-- Name: galaxy; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.galaxy (
    galaxy_id integer NOT NULL,
    name character varying(30) NOT NULL,
    description text,
    age_in_billions_of_years numeric(5,1),
    galaxy_types text
);


ALTER TABLE public.galaxy OWNER TO freecodecamp;

--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.galaxy_galaxy_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.galaxy_galaxy_id_seq OWNER TO freecodecamp;

--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.galaxy_galaxy_id_seq OWNED BY public.galaxy.galaxy_id;


--
-- Name: moon; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.moon (
    moon_id integer NOT NULL,
    name character varying(30) NOT NULL,
    description text,
    has_life boolean,
    is_spherical boolean,
    planet_id integer
);


ALTER TABLE public.moon OWNER TO freecodecamp;

--
-- Name: moon_moon_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.moon_moon_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.moon_moon_id_seq OWNER TO freecodecamp;

--
-- Name: moon_moon_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.moon_moon_id_seq OWNED BY public.moon.moon_id;


--
-- Name: planet; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.planet (
    planet_id integer NOT NULL,
    name character varying(30) NOT NULL,
    description text,
    has_life boolean,
    is_spherical boolean,
    distance_from_earth numeric(5,2),
    age_in_billions_of_years numeric(5,2),
    star_id integer
);


ALTER TABLE public.planet OWNER TO freecodecamp;

--
-- Name: planet_planet_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.planet_planet_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.planet_planet_id_seq OWNER TO freecodecamp;

--
-- Name: planet_planet_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.planet_planet_id_seq OWNED BY public.planet.planet_id;


--
-- Name: star; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.star (
    star_id integer NOT NULL,
    name character varying(30) NOT NULL,
    description text,
    has_life boolean,
    is_spherical boolean,
    galaxy_id integer,
    temperature_in_kelvins integer
);


ALTER TABLE public.star OWNER TO freecodecamp;

--
-- Name: star_star_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.star_star_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.star_star_id_seq OWNER TO freecodecamp;

--
-- Name: star_star_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.star_star_id_seq OWNED BY public.star.star_id;


--
-- Name: black_hole black_hole_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.black_hole ALTER COLUMN black_hole_id SET DEFAULT nextval('public.black_hole_black_hole_id_seq'::regclass);


--
-- Name: galaxy galaxy_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy ALTER COLUMN galaxy_id SET DEFAULT nextval('public.galaxy_galaxy_id_seq'::regclass);


--
-- Name: moon moon_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon ALTER COLUMN moon_id SET DEFAULT nextval('public.moon_moon_id_seq'::regclass);


--
-- Name: planet planet_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet ALTER COLUMN planet_id SET DEFAULT nextval('public.planet_planet_id_seq'::regclass);


--
-- Name: star star_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star ALTER COLUMN star_id SET DEFAULT nextval('public.star_star_id_seq'::regclass);


--
-- Data for Name: black_hole; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.black_hole VALUES ('Sagitarrius A', 2018, 1, 1, 'Supermassive black hole at center of milky way');
INSERT INTO public.black_hole VALUES ('Fornax A', 1970, NULL, 2, 'Supermassive black hole');
INSERT INTO public.black_hole VALUES ('Messier 31', 964, 2, 3, 'ie andromeda galaxy');
INSERT INTO public.black_hole VALUES ('messier 104', 1781, NULL, 4, 'Unclear classification');
INSERT INTO public.black_hole VALUES ('Arp 220', 1987, NULL, 5, 'Ultraluminous infrared galaxy');
INSERT INTO public.black_hole VALUES ('V Puppis', 999, NULL, 6, 'Likely a black hole');


--
-- Data for Name: galaxy; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.galaxy VALUES (1, 'Milky Way', 'Includes the solar system', 13.6, 'Barred Spiral Galaxy');
INSERT INTO public.galaxy VALUES (2, 'Andromeda Galaxy', 'Will collide with the Milky Way in 4-5 billion years.', 5.0, 'Barred Spiral');
INSERT INTO public.galaxy VALUES (3, 'Messier 82', 'Closest starburst galaxy to the Milky Way', 999.0, 'Starburst');
INSERT INTO public.galaxy VALUES (4, 'NHC 7814', 'The Little Sombrero', 999.0, 'Spiral');
INSERT INTO public.galaxy VALUES (5, 'Hoags Object', 'Discovered in 1950', 999.0, 'Ring');
INSERT INTO public.galaxy VALUES (6, 'NGC 4565', 'In coma berenices constellation', 999.0, 'Spiral');
INSERT INTO public.galaxy VALUES (7, 'NGC 7479', 'In constellation Pegasus', 999.0, 'Barred spiral');


--
-- Data for Name: moon; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.moon VALUES (1, 'Moon', 'The only natural satellite of Earth.', false, true, 1);
INSERT INTO public.moon VALUES (2, 'Phobos', 'Rubble pile', false, false, 2);
INSERT INTO public.moon VALUES (3, 'Deimos', 'May escape Mars gravity', false, false, 2);
INSERT INTO public.moon VALUES (4, 'Europa', 'Super smooth ice moon', false, true, 3);
INSERT INTO public.moon VALUES (5, 'Ganymede', 'Would be considered planet if revolved around sun', false, true, 3);
INSERT INTO public.moon VALUES (6, 'Prometheus', 'Shephard mooon', false, true, 4);
INSERT INTO public.moon VALUES (7, 'Callisto', 'Discovered by Galileo in 1610', false, true, 3);
INSERT INTO public.moon VALUES (8, 'Kale', 'Discovered in 2001', false, false, 3);
INSERT INTO public.moon VALUES (9, 'Leda', 'Discovered in 1974', false, false, 3);
INSERT INTO public.moon VALUES (10, 'Metis', 'Discovered in 1979', false, false, 3);
INSERT INTO public.moon VALUES (11, 'Atlas', 'Discovered in 1980', false, false, 4);
INSERT INTO public.moon VALUES (12, 'Helene', 'One of the four Trojan moons', false, true, 4);
INSERT INTO public.moon VALUES (13, 'Narvi', 'Named after a Norse giant', false, true, 4);
INSERT INTO public.moon VALUES (14, 'Skathi', 'Discovered in 2006', false, false, 4);
INSERT INTO public.moon VALUES (15, 'Tarvos', 'Member of the Gaulic group', false, false, 4);
INSERT INTO public.moon VALUES (16, 'Charon', 'Largest of the Pluto moons', false, false, 7);
INSERT INTO public.moon VALUES (17, 'Nix', 'Named after the goddess of night', false, false, 7);
INSERT INTO public.moon VALUES (18, 'Hydra', 'Second largest moon of Pluto', false, false, 7);
INSERT INTO public.moon VALUES (19, 'Kerberos', 'Double lobed', false, false, 7);
INSERT INTO public.moon VALUES (20, 'Styx', 'Discovered in 2012', false, false, 7);


--
-- Data for Name: planet; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.planet VALUES (1, 'Earth', 'Humans! Home!', true, true, 0.00, 4.55, 3);
INSERT INTO public.planet VALUES (2, 'Mars', 'Fourth planet from the sun.', false, true, 33.90, 4.60, 3);
INSERT INTO public.planet VALUES (3, 'Jupiter', 'Fifth planet from the Sun', false, true, 367.00, 4.50, 3);
INSERT INTO public.planet VALUES (4, 'Saturn', 'Nine earth diameters', false, true, 967.00, 999.00, 3);
INSERT INTO public.planet VALUES (5, 'Uranus', 'Ice giant', false, true, 999.00, 999.00, 3);
INSERT INTO public.planet VALUES (6, 'Neptune', 'Densest giant planet in solar system', false, true, 999.00, 999.00, 3);
INSERT INTO public.planet VALUES (7, 'Pluto', 'Dwarf planet', false, true, 999.00, 999.00, 3);
INSERT INTO public.planet VALUES (8, 'Mercury', 'Fastest planet', false, true, 999.00, 999.00, 3);
INSERT INTO public.planet VALUES (9, 'Venus', 'Earths sister', false, true, 999.00, 999.00, 3);
INSERT INTO public.planet VALUES (10, 'Kepler 90 H', 'Revolves Around Kepler 90', false, true, 999.00, 999.00, 7);
INSERT INTO public.planet VALUES (11, 'Kepler 90 G', 'Revolves around Kepler 90', false, true, 999.00, 999.00, 7);
INSERT INTO public.planet VALUES (12, 'Kepler 90 F', 'Revolves Around Kepler 90', false, true, 999.00, 999.00, 7);


--
-- Data for Name: star; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.star VALUES (1, 'Stephenson 2 DFK 1', 'Red Supergiant. Largest in Milky Way', false, true, 1, 3200);
INSERT INTO public.star VALUES (3, 'The Sun', 'The center of the solar system', false, true, 1, 5800);
INSERT INTO public.star VALUES (4, 'Sirius', 'The brightest star in our night sky.', false, true, 1, 25000);
INSERT INTO public.star VALUES (5, 'Alpha Andromeda', 'Brightest star in Andromeda constellation', false, true, 2, 13800);
INSERT INTO public.star VALUES (6, 'Epsilon Pegasi', 'Red supergiant', false, true, 7, 4000);
INSERT INTO public.star VALUES (7, 'Kepler 90', 'In the Draco constellation', false, true, 1, 6080);


--
-- Name: black_hole_black_hole_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.black_hole_black_hole_id_seq', 6, true);


--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.galaxy_galaxy_id_seq', 7, true);


--
-- Name: moon_moon_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.moon_moon_id_seq', 20, true);


--
-- Name: planet_planet_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.planet_planet_id_seq', 12, true);


--
-- Name: star_star_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.star_star_id_seq', 7, true);


--
-- Name: black_hole black_hole_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.black_hole
    ADD CONSTRAINT black_hole_name_key UNIQUE (name);


--
-- Name: black_hole black_hole_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.black_hole
    ADD CONSTRAINT black_hole_pkey PRIMARY KEY (black_hole_id);


--
-- Name: galaxy galaxy_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy
    ADD CONSTRAINT galaxy_name_key UNIQUE (name);


--
-- Name: galaxy galaxy_name_key1; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy
    ADD CONSTRAINT galaxy_name_key1 UNIQUE (name);


--
-- Name: galaxy galaxy_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy
    ADD CONSTRAINT galaxy_pkey PRIMARY KEY (galaxy_id);


--
-- Name: moon moon_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_name_key UNIQUE (name);


--
-- Name: moon moon_name_key1; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_name_key1 UNIQUE (name);


--
-- Name: moon moon_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_pkey PRIMARY KEY (moon_id);


--
-- Name: planet planet_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_name_key UNIQUE (name);


--
-- Name: planet planet_name_key1; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_name_key1 UNIQUE (name);


--
-- Name: planet planet_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_pkey PRIMARY KEY (planet_id);


--
-- Name: star star_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_name_key UNIQUE (name);


--
-- Name: star star_name_key1; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_name_key1 UNIQUE (name);


--
-- Name: star star_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_pkey PRIMARY KEY (star_id);


--
-- Name: black_hole black_hole_galaxy_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.black_hole
    ADD CONSTRAINT black_hole_galaxy_id_fkey FOREIGN KEY (galaxy_id) REFERENCES public.galaxy(galaxy_id);


--
-- Name: moon moon_planet_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_planet_id_fkey FOREIGN KEY (planet_id) REFERENCES public.planet(planet_id);


--
-- Name: planet planet_star_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_star_id_fkey FOREIGN KEY (star_id) REFERENCES public.star(star_id);


--
-- Name: star star_galaxy_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_galaxy_id_fkey FOREIGN KEY (galaxy_id) REFERENCES public.galaxy(galaxy_id);


--
-- PostgreSQL database dump complete
--

