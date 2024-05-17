<script lang="ts">
  import {
    Container,
    Row,
    Col,
    Progress,
} from '@sveltestrap/sveltestrap'
</script>

<h1 class="text-3xl font-bold underline">
  Hello world!
</h1>

<Container fluid>
  <h3 class="container">container fluid</h3>
</Container>

<Container sm>
  <h3 class="container">container sm</h3>
</Container>

<Container md>
  <h3 class="container">container md</h3>
</Container>

<Container lg>
  <h3 class="container">container lg</h3>
</Container>

<Container xl>
  <h3 class="container">container xl</h3>
</Container>

<Container xxl>
  <h3 class="container">container xxl</h3>
</Container>

<Container>
  <Row>
    <Col>.col</Col>
  </Row>
  <Row>
    <Col>.col</Col>
    <Col>.col</Col>
    <Col>.col</Col>
    <Col>.col</Col>
  </Row>
  <Row>
    <Col xs="3">.col-3</Col>
    <Col xs="auto">.col-auto - variable width content</Col>
    <Col xs="3">.col-3</Col>
  </Row>
  <Row>
    <Col xs="6">.col-6</Col>
    <Col xs="6">.col-6</Col>
  </Row>
  <Row>
    <Col xs="6" sm="4">.col-6 .col-sm-4</Col>
    <Col xs="6" sm="4">.col-6 .col-sm-4</Col>
    <Col sm="4">.col-sm-4</Col>
  </Row>
  <Row>
    <Col sm={{ size: 6, order: 2, offset: 1 }}>
      .col-sm-6 .order-sm-2 .offset-sm-1
    </Col>
  </Row>
  <Row>
    <Col sm="12" md={{ size: 6, offset: 3 }}>
      .col-sm-12 .col-md-6 .offset-md-3
    </Col>
  </Row>
  <Row>
    <Col sm={{ size: 'auto', offset: 1 }}>.col-sm-auto .offset-sm-1</Col>
    <Col sm={{ size: 'auto', offset: 1 }}>.col-sm-auto .offset-sm-1</Col>
  </Row>
  <Row cols={2}>
    <Col>col-1</Col>
    <Col>col-2</Col>
    <Col>col-3</Col>
    <Col>col-4</Col>
    <Col>col-5</Col>
    <Col>col-6</Col>
  </Row>
  <Row cols={{ lg: 3, md: 2, sm: 1 }}>
    <Col>col-1</Col>
    <Col>col-2</Col>
    <Col>col-3</Col>
    <Col>col-4</Col>
    <Col>col-5</Col>
    <Col>col-6</Col>
  </Row>
</Container>

<Progress value={25} class="mb-2">25%</Progress>
<Progress value={50} class="mb-2">1/2</Progress>
<Progress value={75} class="mb-2">You're almost there!</Progress>
<Progress color="success" value={100} class="mb-2">You did it!</Progress>

<Progress multi class="mb-2">
  <Progress bar value={15}>Meh</Progress>
  <Progress bar color="success" value={30}>Wow!</Progress>
  <Progress bar color="info" value={25}>Cool</Progress>
  <Progress bar color="warning" value={20}>20%</Progress>
  <Progress bar color="danger" value={5}>!!</Progress>
</Progress>

<Progress striped value={2 * 5} class="mb-2" />
<Progress striped color="success" value={25} class="mb-2" />
<Progress striped color="info" value={50} class="mb-2" />
<Progress striped color="warning" value={75} class="mb-2" />
<Progress striped color="danger" value={100} class="mb-2" />

<Progress multi class="mb-2">
  <Progress striped bar value={10} />
  <Progress striped bar color="success" value={30} />
  <Progress striped bar color="warning" value={20} />
  <Progress striped bar color="danger" value={20} />
</Progress>

<Progress animated value={2 * 5} class="mb-2" />
<Progress animated color="success" value={25} class="mb-2" />
<Progress animated color="info" value={50} class="mb-2" />
<Progress animated color="warning" value={75} class="mb-2" />
<Progress animated color="danger" value={100} class="mb-2" />

<Progress multi class="mb-2">
  <Progress animated bar value={10} />
  <Progress animated bar color="success" value={30} />
  <Progress animated bar color="warning" value={20} />
  <Progress animated bar color="danger" value={20} />
</Progress>

<Progress multi>
  <Progress bar value={15} />
  <Progress bar color="success" value={20} />
  <Progress bar color="info" value={20} />
  <Progress bar color="warning" value={20} />
  <Progress bar color="danger" value={15} />
</Progress>

<Progress multi>
  <Progress bar value={15}>Meh</Progress>
  <Progress bar color="success" value={35}>Wow!</Progress>
  <Progress bar color="warning" value={25}>25%</Progress>
  <Progress bar color="danger" value={25}>LOOK OUT!!</Progress>
</Progress>

<Progress multi>
  <Progress bar striped value={15}>Stripes</Progress>
  <Progress bar animated color="success" value={30}>Animated Stripes</Progress>
  <Progress bar color="info" value={25}>Plain</Progress>
</Progress>

<Progress value={1} max={5} />
<Progress value={50} max={135} />
<Progress value={75} max={111} />
<Progress value={463} max={500} />

<Progress multi>
  <Progress bar value={5} max={55}>5</Progress>
  <Progress bar color="success" value={15} max={55}>15</Progress>
  <Progress bar color="warning" value={10} max={55}>10</Progress>
  <Progress bar color="danger" value={10} max={55}>10</Progress>
</Progress>

<div class="text-content">Dark Theme</div>
<Progress theme="dark" value={25} class="mb-2">25%</Progress>
<Progress theme="dark" striped value={2 * 5} class="mb-2" />
<Progress theme="dark" animated value={2 * 5} class="mb-2" />

<div class="text-content">Light Theme</div>
<Progress theme="light" value={25} class="mb-2">25%</Progress>
<Progress theme="light" striped value={2 * 5} class="mb-2" />
<Progress theme="light" animated value={2 * 5} class="mb-2" />
<style lang="postcss">
  :global(html) {
    background-color: theme(colors.gray.100);
  }
</style>